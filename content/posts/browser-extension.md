---
title: "Nhập môn Browser extension"
date: 2025-02-19T00:29:44+07:00
tags: ["browser-extension", "code"]
# draft: true
---

Chuyện là mình có hứa với thằng bạn mình viết 1 bài về cách làm browser extension, và cũng như mình có ý tưởng là làm 1 cái extension để tìm nhiều thứ cùng 1 lúc, nên mình viết bài này, win-win.

Ý tưởng của extension: Chuyện là mình có làm 1 cái extension [Dictionary Look Up](https://github.com/ngntrgduc/Dictionary-Look-Up) để search từ điển tiếng Anh nhanh hơn. Nó chỉ có chức năng là search từ vựng cho các trang được định sẵn thôi. Mình muốn search Google (hoặc những trang khác nhau, như cái chức năng Vomnibar của [Vimium](https://ngntrgduc.github.io/posts/vimium/)) nhiều cái (cùng 1 lúc), thông qua dấu `,` để đỡ phải `Ctrl + T` nhiều lần. Do Vomnibar của Vimium không hoạt động được khi đang ở tab có file pdf, mà extension lại có thể, nên cái extension này ra đời 🐣.

Có nhiều frameworks hỗ trợ việc viết extension đơn giản hơn, cross platforms các kiểu luôn, nhưng vì mình lười và sự khác biệt giữa code cho Chome (Chromium) và Firefox là không đáng kể nên mình không dùng framework, cho nó máu 🩸.

Để đọc bài này thì bạn chỉ cần kiến thức cơ bản về HTML, CSS và một chút JS (bao gồm JSON) là được. Và chỉ cần với 3-4 files thì bạn đã có thể làm được một cái browser extension đơn giản để nghịch rồi.

Note: Do mình chưa xài máy Mac bao giờ 🥲, nên bài viết này chỉ tập trung Chrome với Firefox thôi nha.

### Cấu trúc của browser extension
Hiểu đơn giản browser extension là 1 cái web được thu nhỏ lại thôi. Dĩ nhiên cũng có những extension không cần CSS hay JS, nhưng web mà không có CSS nhìn rất xấu và không có JS thì không làm được nhiều trò hay ho.

Cấu trúc cơ bản của extension ta sẽ làm:
- `index.html`: gồm cái thanh search bar
- `style.css`: làm cho cái thanh search bar đẹp hơn, có cảm hứng để xài hơn
- `script.js`: script để xử lí nội dung search rồi mở nhiều tabs, và làm thêm nhiều trò hay ho khác...
- **`manifest.json`**: cung cấp các thông tin cần thiết, các quyền hạn cho extension. Phải có cái file này thì browser mới hiểu cái thư mục hiện tại là 1 cái extension, rồi load thư mục đó dưới dạng extension

### Vào cuộc

Tạo folder mới với lần lượt các file:

**`index.html`**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Multiple Search</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <input id="searchBox" maxlength="50" autofocus>
</body>
<script src="script.js"></script>
</html>
```

File này chill, gồm cái tag input để nhập chữ, và link với file CSS và JS.

**`style.css`**
```css
body {
    width: 370px;
    margin: 15px 0;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
}

input {
    padding: 8px;
    font-size: 16px;
    border: 1px solid silver;
    border-radius: 8px;
    background-color: white;
    font-family: Arial, Helvetica, sans-serif;
    color: #303030;
}

input:focus {
    outline: 0;
    border-color: #95c0fe;
    box-shadow: 0 0 0 0.2em #c2daff;
}
```

Cái này mình ~~ăn cắp~~ tham khảo ý tưởng của framework Bootstrap. Và đây là thành quả:

![](/browser_extension/extension.png)

Nnìn hơi dài, các bạn có thể chỉnh cho nó nhỏ lại nếu các bạn muốn.

**`script.js`**
```js
const searchBox = document.getElementById("searchBox");

document.addEventListener("DOMContentLoaded", () => {
    setTimeout(() => {
        if (document.activeElement !== searchBox) {
            searchBox.focus(); // Workaround for Firefox autofocus
        }
    }, 10)
})

function format(word) {
    return word.trim().replaceAll(" ", "+");
}

function search(word) {
    if (!word.trim()) return;
    chrome.tabs.create({ 
        url: "https://www.google.com/search?q=" + format(word)
    });
}

searchBox.addEventListener("keydown", function(e) {
    if (e.key === "Enter") {
        let word = e.target.value.toLowerCase().trim();        
        const delimiter = ",";
        if (word.includes(delimiter)) {
            const words = word.split(",");
            for (word of words) {
                search(word);
            }
        } else {
            search(word);
        }
        window.close();
    }
});
```

Đoạn code thứ 2 mình dùng để fix cái lỗi autofocus của cái input trên Firefox. Nếu bạn sử dụng Chrome thì có thể xoá nó đi. Ở đây, mình dùng `chrome.tabs.create` để tạo tabs mới thông qua API của Chrome.

**Lưu ý:** Chrome Extension API có namespace là `chrome` còn ở Firefox nó là `browser`. 

Rồi, bây giờ biến cái trang web này thành cái extension nào.

**`manifest.json`**

```json
{
    "manifest_version": 3,
    "name": "Multiple Search",
    "version": "0.0.1",
    "description": "Search multiple stuff, blazingly fast",
    "action": {
        "default_popup": "index.html",
        "default_title": "Multiple Search"
    },
    "permissions": [
        "tabs"
    ]
}
```

Đây là các thông tin cần thiết cho extension. Ngoài ra còn có thêm một số cài đặt khác nữa, giúp extension làm được nhiều trò hơn, nhưng ở đây mình chỉ cần nó mở các tabs thôi nên mình cần `permissions` là `tabs`.


Tất cả đã xong, giờ chỉ việc load extension vô mà xài thôi. Riêng đối với trường hợp Firefox thì cần phải cài đặt bằng file `.xpi`, hoặc là cài đặt ở trên Firefox Add-ons, nhưng mình lười up lên đó, nên các bạn dùng Firefox có gì cứ upload private mà xài nhé. Còn đối với Chrome thì chỉ cần:
1. Vô Settings -> Extensions.
2. Bật Developer mode. 
3. Nhấp `Load unpacked` và chọn cái folder bạn vừa làm.


Kết quả:

![](/browser_extension/final.png)

Một vài ý tưởng hay ho để thêm vô: 
- Tích hợp [brace expansion](https://www.gnu.org/software/bash/manual/html_node/Brace-Expansion.html), tiết kiệm thời gian với những lúc cần lặp từ
- Cảnh báo nếu có nhiều số lượng tabs được tạo ra (có thể là do lỡ tay paste đoạn nào mà có nhiều dấu `,` quá), không thì chỉ cho phép search `n` từ trong 1 lần thôi, đỡ lag máy. Việc đặt `maxlength` ở input có vẻ không khả thi cho lắm...
- Cài đặt cho nhiều trang web khác nhau. Bạn có thể ~~copy paste~~ tham khảo từ cái Dictionary Look Up của mình, cơ mà mình code hơi ngu nên là đừng chửi mình nhé 🙏

### Resources
- https://developer.chrome.com/docs/extensions
- https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions
- Một vài extension mẫu của Mozilla: https://github.com/mdn/webextensions-examples, nhưng đa số sử dụng manifest version 2. Google khai tử version 2 từ lâu rồi, nhưng vẫn chạy ổn nếu chỉ cần bạn chỉnh 1 vài thứ ở trong cái file `manifest.json` thôi
- https://www.freecodecamp.org/news/building-chrome-extension/, hồi xưa mình học cách làm extension bằng cái blog này
- ~~[Một vài browser extensions mà mình dùng](https://ngntrgduc.github.io/uses/#browser-extension)~~