---
title: "Đọc blog với RSS"
date: 2023-09-05T23:42:11+07:00
tags: ["random"]
---

![](https://images.ctfassets.net/lzny33ho1g45/1M3ZeUX3Y002aMRN6EGzlb/231459741e1ced7c42ad306098572f9d/rss_hero_image.png "icon RSS như này nè")
Có ai đã từng có rất nhiều blog hay, nhưng lại quá mệt mỏi khi phải nhớ tên miền của từng blog, hay phải lưu link lại để lâu lâu vô coi coi có bài mới không chưa? Bạn có thể chỉ cần ngồi im một chỗ và những bài mới sẽ hiện lên trước mắt bạn với RSS.

# RSS là gì?
> RSS (Really Simple Syndication) is a web feed that allows users and applications to access updates to websites in a standardized, computer-readable format. Subscribing to RSS feeds can allow a user to keep track of many different websites in a single news aggregator, which constantly monitor sites for new content, **removing the need for the user to manually check them**. News aggregators (or "RSS readers") can be built into a browser, installed on a desktop computer, or installed on a mobile device.
>
> Websites usually use RSS feeds to publish frequently updated information, such as blog entries, news headlines, episodes of audio and video series, or for distributing podcasts. An RSS document (called "feed", "web feed", or "channel") includes full or summarized text, and metadata, like publishing date and author's name. RSS formats are specified using a generic XML file.
> 
> Wikipedia

Bản dịch nhà làm: RSS là cái web feed (giống cái newsfeed trên Facebook ~~nhưng không có quảng cáo~~) cho phép người dùng có thể biết được những cập nhật mới của nhiều trang web khác nhau, không cần phải check bằng tay nữa.

# Dùng gì để đọc RSS
Để đọc được RSS thì bạn cần phải có RSS reader. Có rất nhiều open-source RSS reader như: [Miniflux](https://github.com/miniflux/v2), [Newsboat](https://github.com/newsboat/newsboat), [FreshRSS](https://github.com/FreshRSS/FreshRSS),... Nhưng khổ nỗi mình dùng Windows, nên giấc mơ RSS của mình bay đi luôn... Ngoài ra mình cũng dùng một số extension RSS trên trình duyệt (hình như trình duyệt Brave nó có tích hợp cả RSS reader luôn) nhưng mà mình thấy nó ngu quá nên cũng từ bỏ...

Nhưng gần đây mình mới phát hiện ra là [Thunderbird](https://www.thunderbird.net/en-US/) cũng có hể dùng để đọc RSS feed. Nó là email client nhưng cũng có thể dùng để đọc RSS. Bạn có thể coi cách setup ở [đây](https://support.mozilla.org/en-US/kb/how-subscribe-news-feeds-and-blogs).

Để có được link RSS của trang web thì bạn coi coi trang web có cái biểu tượng của RSS không, nếu không thì bạn `Ctrl + U` để coi source của web rồi `Ctrl + F` tìm kiếm `rss` hay là `.xml` thử, nếu không có thì trang web đó không có hỗ trợ RSS và bạn phải check web đó bằng tay 🥲.

---

**PS**: trong thời gian viết bài này, khi lướt kĩ cái wikipedia về RSS thì mình mới phát hiện ra là có đoạn nó ghi là RSS có thể được đọc với email client như Thunderbird 🙂:
> "There are various news aggregator software for desktop and mobile devices, but RSS can also be built-in inside web browsers or **email clients like Mozilla Thunderbird**."
>
> Wikipedia

**PPS**: blog của mình cũng có RSS đó nha :>, vô [trang chủ](https://ngntrgduc.github.io/) hay là vô cái [/post](https://ngntrgduc.github.io/posts/) là có :>.
