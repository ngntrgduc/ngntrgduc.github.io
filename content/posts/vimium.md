---
title: "Mình dùng Vimium thế nào?"
date: 2024-02-14T11:01:28+07:00
tags: ["browser-extension", "use"]
---

## Vimium?
[Vimium](https://vimium.github.io/) là một open source extension giúp bạn duyệt
web mà không cần chuột, và tuỳ chỉnh các phím tắt của riêng bạn khi duyệt web.

Mặc dù Vimium lấy ý tưởng các phím tắt từ Vim - text editor dành cho dân coder,
nhưng mình thấy mọi người đều có thể sử dụng, tuỳ chỉnh theo ý thích của mình. 
Chỉ là với những người biết xài Vim rồi thì xài Vimium sẽ quen tay hơn thôi.

## Lý do xài
Do hồi xưa con chuột của mình bị hư, trackpad của em laptop "giả" gaming (ý mình
là nó nặng như con laptop gaming) Core i3 RAM 4GB đã cũ, không còn mượt, và mình
cũng mới tập tành Vim nên tín hiệu vũ trụ đưa mình tới cái extension này. Xài
được một thời gian thì thấy nó tiện phết, nhất là với mấy đứa không xài chuột
như mình.


## Những tính năng
Mình kiếm không ra cái video nào giới thiệu Vimium đủ hay và ngắn, cái video giới thiệu của tác giả thì quá cũ (từ 10 mấy năm trước), trên mạng có đầy những bài viết nói về tính năng của nó rồi, ~~và do mình lười~~ nên mình sẽ liệt kê mấy tính năng hữu ích (đã được mình mapping lại) mà mình đang dùng thôi nhé:

- Di chuyển lên xuống bằng `h`, `j`, `u`, `d`
- Chuyển qua tab kế bên bằng `J`, `K`
- Quay lại, tiến tới lịch sử của tab hiện tại bằng `H`, `L`
- Di chuyển lên đầu trang web bằng `gg` và di chuyển tới cuối trang web bằng `G`
- Mở link bằng `f`, `F` và mở 1 lúc nhiều links bằng `Alt + f`
- Mở/search cái bạn vừa copy ở tab hiện tại bằng `p` và trong tab mới bằng `P`. Kiểu đang đọc blog, thấy định nghĩa lạ quá thì giờ bạn chỉ cần copy nó rồi gõ `p` hoặc `P` thì nó sẽ Google cho bạn (và bạn cũng có thể đặt search engine mặc định khác như à DuckDuckGo luôn) 
- Reload lại tab hiện tại bằng `r`
- Copy URL của tab hiện tại bằng `yy`
- Đóng tab hiện tại bằng `x`, mở lại tab vừa đóng bằng `X`
- Focus tới cái thanh input trên trang web bằng `gi`, nếu có nhiều thanh input thì dùng `Tab` để chuyển.
- Duplicate tab `yt`, Pin tab `Alt + p`. Một số browser có phím tắt để làm những việc này nhưng Firefox thì không có 🥲, nên cái này tiện lợi x100
- Chuyển mục nhanh hơn với `[[`, `]]`. Ví dụ như với trang https://d2l.ai/, thay vì mỗi lần đọc xong một mục nhỏ trong một chapter, bạn muốn chuyển qua mục tiếp theo thì bạn cần nhấn vô cái chuyển mục ở cuối trang hoặc nhấn vô mục tiếp theo ở mục lục phía bên trái. Nhưng với Vimium thì bạn chỉ cần `]]` là đã có thể đi tới mục tiếp theo hoặc `[[` để trở về mục trước đó. Nhưng với điều kiện là phải đúng với label ở trong settings nhé.
- Vomnibar: Nó đóng vai trò như cái thanh URL/search của browser ấy, nhưng nó còn [làm được nhiều thứ](#vomnibar) hơn thế.

Ngoài ra còn nhiều tính năng khác nữa, bạn có thể tham khảo tại trang web của extension.

**Hạn chế**: 1 điều đáng buồn là khi mở pdf ở trong browser thì Vimium không xài được do vấn đề về bảo mật. Ví dụ đang coi pdf ngon lành, gặp từ mới không biết, muốn tra thử thì không thể nhấn `t` để mở tab mới mà phải dùng `Ctrl T` mới được 🥲. Một số phím tắt sử dụng để navigate cũng không sử dụng được luôn 🥲.

## Mình dùng nó như thế nào?

Bạn có thể tìm thấy toàn bộ settings của mình [ở đây](https://gist.github.com/ngntrgduc/56466d9bb66b2d2a7a27d42442a99850/710bf496112d68b09eb83d3b5ae9f026eef4215a)
(phiên bản này sẽ cũ theo thời gian, nhưng bạn vẫn có thể coi được những phiên
bản mới nhất trong gist này), với những tuỳ chỉnh phù hợp với nhu cầu của mình,
bạn đọc kĩ hướng dẫn sử dụng trước khi dùng nhé.

### Theme
Cái theme mặc định của Vimium quá phèn nên mình tự custom theme.  Theme của mình
làm lấy theme [Catppuccin](https://github.com/catppuccin/catppuccin) làm chủ đạo
(Vâng mình là fan của Catppuccin 😸, cả cái blog này cũng có theme Catppuccin). 
Catppuccin cũng có [repo cho Vimium](https://github.com/catppuccin/vimium/) 
nhưng nó làm mình bị đau mắt nên mình chỉnh lại cho mắt của mình đỡ đau.

- Mặc định
    ![](/vimium/f-default.png)
    ![](/vimium/o-default.png)
- Của Catppuccin
    ![](/vimium/f-catppuccin.png)
    ![](/vimium/o-catppuccin.png)
- Của mình
    ![](/vimium/f-mine.png)
    ![](/vimium/o-mine.png)


Theme config của mình nằm [ở đây](https://gist.github.com/ngntrgduc/56466d9bb66b2d2a7a27d42442a99850/710bf496112d68b09eb83d3b5ae9f026eef4215a#file-vimium-theme-js). 
Nếu không thích thì bạn có thể lên GitHub để tìm [theme có sẵn](https://github.com/philc/vimium/wiki/Theme), hoặc bạn cũng có thể hardcore để tạo theme mà mình thích.

### Mapping
**Note**: Mình sử dụng Firefox nên sẽ có những settings phù hợp với Firefox hơn là với Chrome, Edge,... Ví dụ như `/` sẽ mở Quick find trên Firefox, đồng thời nó giúp focus vô cái thanh search trên Youtube, nên mình sẽ unmap toàn bộ Find mode trong Vimium. Với lại dùng `Ctrl + f` cho nhanh đi mọi người 🙂.

Có nhiều mapping không cần thiết nên mình đã unmap nó, và mapping lại 1 số keys:
```
unmap <c-e>
unmap <c-y>
unmap h
unmap l
unmap T
unmap v
unmap V
unmap O
unmap b
unmap B
unmap gt
unmap gT
unmap gs
unmap gf
unmap gF
unmap g0
unmap g$
unmap W
unmap R
unmap ge
unmap gE
unmap zL
unmap zH
unmap /
unmap n
unmap N
unmap ?

map o Vomnibar.activateInNewTab
map gf LinkHints.activateModeToOpenInNewForegroundTab
map R Vomnibar.activateEditUrlInNewTab
map b visitPreviousTab
```

Và nó sẽ như thế này (mình không xài `?` vì mình đã thuộc mấy cái này rồi nhưng mà để demo nên mình mới đặt lại á):

![](/vimium/mapping.png)

Bên cạnh đó, có một số mapping mà mình ít xài như:
- `i`: Kích hoạt insert mode: Insert mode trong Vimium là chế độ bạn có thể gõ gì cũng được mà không kích hoạt các phím tắt của nó. Thường thì khi đang focus vô cái thanh input thì Vimium sẽ không được kích hoạt
- `gu` để lùi về 1 bậc URL và `gU` lùi về tới root của URL của tab hiện tại (nói chung là mình cũng không biết phải diễn tả làm sao hết 🥲).
Ví dụ như mình đang ở tab `https://github.com/ngntrgduc/ngntrgduc.github.io`, thì `gU` sẽ chuyển tab hiện tại thành `https://github.com/` còn `gu` sẽ chỉ chuyển về `https://github.com/ngntrgduc/` thôi
- `gf` Mở link ở tab mới và chuyển qua nó: Mình thưởng mở bằng `F` rồi dùng `K` để nhảy qua luôn
- `yf` Copy link URL vào clipboard
- `m` Create a new mark: Kiểu bạn đọc thấy cái phần ở giữa của cái blog hay quá, bạn muốn đọc xong blog thì quay lại đọc phần ở giữa này tiếp, thì cái tính năng mark này giúp bạn nhảy hẳn tới cái phần bạn vừa mark xong. Thường thì mình kiếm lại luôn chứ không có mark nó lại. Nhưng nó cũng hữu ích trong 1 số trường hợp.
- `^, b` Go to previously-visited tab: Hữu ích với những trường hợp muốn tab qua lại các tab thật là nhanh vì thay vì `Ctrl + Tab`, `Ctrl + Shift + Tab` thì giờ bạn chỉ cần gõ 1 kí tự là đã có thể chuyển tab.
- `R` dùng để chỉnh sửa URL của tab hiện tại và mở nó vào tab mới.
- `<<`, `>>` Bê cái tab hiện tại qua bên trái, phải: Di chuyển bằng con trỏ chuột nhanh hơn.

### Vomnibar
Bạn có thể dùng cái này để search Google, search lại lịch sử, search bookmark,... 
với những kết quả hiện ra thì sử dụng `Tab` để di chuyển...

Lúc mới bắt đầu xài mình thấy cái này kiểu nhảm nhảm làm sao, cần gì một cái
search bar của extension trong khi mình đã có cái search bar của browser rồi?.
Nhưng đó là trước khi mình biết tới cái tính năng Custom [search engines](https://github.com/philc/vimium/wiki/Search-Engines) của nó.

Lấy ví dụ cho dễ hiểu nè: Giả sử mình đang nghe nhạc trên Youtube, thấy bài đang
nghe hay quá, mình muốn check thử coi trên Soundcloud có bài này không để like
rồi nghe sau (vì Soundcloud không có ads). Thì mình phải mở tab mới, gõ trang
chủ của soundcloud, nhấn Enter, đợi nó load, rồi vô cái search box, gõ tên của
cái bài hát mình đang nghe trên Youtube, rồi nhấn Enter... Nhưng với Vomnibar và
search engine, giờ mình chỉ cần mở nó lên bằng `o`, gõ `sc` (vì mình đặt cái này
là shorcut cho Soundcloud), nhấn space để kích hoạt search engine, gõ tên bài
hát và nhấn Enter thì ngay lúc này mình đã có thể xem được bài hát đó có trên 
Soundcloud hay không rồi, rất tiết kiệm thời gian 😘.

Nó còn làm được nhiều thứ hơn ví dụ như là search từ vựng các kiểu nữa cơ. Nói chung là phải dùng thì mới thấy được sự tiện lợi của nó.

Dưới đây là một số custom search engine của mình:
```
sc: https://soundcloud.com/search?q=%s SoundCloud
gh: https://github.com/search?q=%s&type=repositories GitHub
y: https://www.youtube.com/results?search_query=%s YouTube
tt: http://tratu.soha.vn/dict/en_vn/%s Tra từ
lw: https://app.ludwig.guru/s/%s Ludwig
lg: https://libgen.is/search.php?&req=%s&sort=extension&sortmode=DESC LibGen
exact: https://www.google.com/search?q="%s" Search for an exact match
urban: https://www.urbandictionary.com/define.php?term=%s Urban Dictionary
yg: https://youglish.com/pronounce/%s/english? YouGlish
oz: https://ozdic.com/collocation/%s/ OZDIC
```

**Góc PR**: Mình không thêm mấy cái từ điển Anh-Anh như Cambridge hay Oxford vào Vomnibar vì mình dùng cái [extension nhà làm](https://github.com/ngntrgduc/Dictionary-Look-Up) của mình rồi. Nó tiện hơn cái Vomnibar ở chỗ là nó có thể mở được khi đang đọc file pdf luôn nhưng điểm trừ là nó chỉ mở được có 3 cái từ điển mặc định thôi, mặc dù với mình như vậy là đủ xài rồi (nào rảnh mình thêm tính năng custom từ điển sau 🥲).

Dù sao thì đây là settings cho 3 cái từ điển:
```
c: https://dictionary.cambridge.org/dictionary/english/%s Cambridge
ox: https://www.oxfordlearnersdictionaries.com/definition/english/%s Oxford
mw: "https://www.merriam-webster.com/dictionary/%s Merriam-Webster
```

### Một số thứ khác
Mình chỉnh scroll step size lên `80px` cho nhanh, characters sử dụng cho link
hints là `sdfghjkl` vì mấy đứa này nằm trên home row, dễ gõ, và mình bỏ `a` vì
`a` gõ thêm `s`, `f`, `j` trong chế độ Telex nó sẽ ra `á`, `à`, `ạ`, và sẽ không
thể thực hiện tiếp link hint 🥲. Điều tương tự cũng xảy ra với Vomnibar (`o`),
lúc này bạn có thể xoá đi rồi gõ lại (giống như Soundcloud là `sc`, mình mở
Vomnibar lên xong phải xoá đi rồi mới gõ tiếp `sc` chứ không nó sẽ ra chữ `óc`
🥲), hoặc là bạn có thể đặt 1 cái shortcut khác để mở Vomnibar, hoặc là chuyển
qua VNI...

Và đôi lúc bạn không muốn dùng Vimium cho mấy trang web như Messenger,... thì
bạn có thể exclude cái URL của nó hoặc chỉ exclude một số keys nhất định thôi.
Ví dụ như với Youtube thì mình exclude `i><1234567890/m` vì nó cũng là phím tắt
mặc định của Youtube, bạn có thể tìm hiểu thêm về phím tắt của Youtube [ở đây](https://www.mrfdev.com/youtube-keyboard-shortcuts).

## Lời kết
Lời khuyên của mình là các bạn hãy cứ cài Vimium vô browser, sử dụng theo những
cái mặc định trước, không cần thiết phải làm theo mình. Nếu thấy cái nào không
cần thiết thì bạn cứ chỉnh sau cũng được. Ngoài ra thì cái [Wiki của Vimium](https://github.com/philc/vimium/wiki) cũng khá là đầy đủ nếu bạn muốn
tận dụng hết tính năng của nó.

Nhìn chung thì Vimium tiết kiệm được cho mình khá nhiều thời gian, và mình mong
rằng nó cũng sẽ tiết kiệm được thời gian cho bạn 💖.