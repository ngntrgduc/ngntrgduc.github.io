---
title: "Chuyển nhà tới Hugo"
date: 2023-07-25
tags: ["random"]
math: true
---

Vô tình lướt qua được video giới thiệu Hugo của [Luke Smith](https://www.youtube.com/watch?v=ZFL09qhKi5I), cộng thêm việc cái [blog cũ](https://github.com/ngntrgduc/old-blog) của mình nhìn cứ chậm chậm, bị glitch khi navigate, và mỗi lần chỉnh cái gì thì mình toàn làm trên GitHub 🥲 (mình viết bài, add file rồi push lên GitHub chứ chưa từng chạy code live server bao giờ),... Và cuối cùng là cái theme [PaperMod](https://github.com/adityatelange/hugo-PaperMod) mượt mà quá 🤯, Hugo lại smooth smooth nữa, nên là mình quyết định chuyển nhà qua đây. Mong là chuyển nhà xong sẽ siêng đăng bài hơn 🥲.

```python
print('Hello Hugo 🔥')
```
---

**PS**: mình mất ~1 buổi chiều để chuyển qua Hugo và mất 1 buổi tối + 1 buổi sáng cho việc fix cái lỗi render $\LaTeX$ trên cái theme này 🙂.

![fix-math](/fix-math.png "Rất nhiều lần fix bug...")

**PPS**: nếu ai muốn render $\LaTeX$ trên cái theme PaperMod này thì bạn phải tạo file 
`layouts\partials\extend_head.html` (nhớ là tạo ở thư mục gốc chứ đừng có vô chỉnh ở cái `themes\PaperMod` nha). Rồi paste cái này vô `extend_head.html`:

```html
{{ if or .Params.math .Site.Params.math }}
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.12.0/dist/katex.min.css" integrity="sha384-AfEj0r4/OFrOo5t7NnNe46zW/tFgW6x/bCJG8FqQCEo3+Aro6EYUG4+cU+KJWu/X" crossorigin="anonymous">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.12.0/dist/katex.min.js" integrity="sha384-g7c+Jr9ZivxKLnZTDUhnkOnsh30B4H0rpLUpJ4jAIKs4fnJI+sEnkvrMWph2EDg4" crossorigin="anonymous"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.12.0/dist/contrib/auto-render.min.js" integrity="sha384-mll67QQFJfxn0IYznZYonOWZ644AWYC+Pt2cHqMaRhXVrursRwvLnLaebdGIlYNa" crossorigin="anonymous"
    onload="renderMathInElement(document.body, 
    {
              delimiters: [
                  {left: '$$', right: '$$', display: true},
                  {left: '\\[', right: '\\]', display: true},
                  {left: '$', right: '$', display: false},
                  {left: '\\(', right: '\\)', display: false}
              ]
          }
    );"></script>
{{ end }}
```