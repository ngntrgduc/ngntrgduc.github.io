---
title: "Từ bỏ Deep learning"
date: 2024-03-09T10:11:33+07:00
tags: ["deep learning"]
# draft: true
---

{{< figure align=center src="/dl/dl.jpg" width="300px" >}}


> Có lẽ mình không hợp với Deep learning?

Đây là câu hỏi mà mình nhớ là nó đã có trong đầu mình từ lâu lắm rồi, chắc là tầm lúc mình đang năm 2 gì đấy. Mình nghĩ câu hỏi này chỉ là câu hỏi ngu thôi nhưng chắc là mình đã sai.

Kì trước mình có học môn Nhận dạng mẫu (Pattern recognition and Machine learning), và đợt này có rất nhiều cái lần đầu của mình:
- Lần đầu Pytorch
- Lần đầu Hugging Face
- Lần đầu overfiting
- Lần đầu finetune model
- Lần đầu hyperparameter tuning
- Lần đầu chạy CNN, RNN ~~nhưng chả hiểu cái gì đang xảy ra~~
- ...

Khi làm lab của môn này, cảm giác vui mừng khi con model của mình chạy không phải đến từ sự thích thú với Deep learning (DL) mà là vì con model của mình chạy được và mong rằng điểm của mình sẽ không thấp 🙂. Và thần kì là nó không thấp thật, em cảm ơn thầy rất nhiều 🥲.

Học xong mình mới phát hiện rằng hoá ra mình không hợp với DL cho lắm, hay nói đúng hơn là mình không học nổi DL. Mình nghĩ chắc cũng phải tới lúc dừng lại và kiếm gì khác để học/làm.

Lý do từ bỏ?
- Mình ~~ngu~~ gà. Mình có thể ngồi tới 1, 2h sáng để đọc toán, hoặc là fix mấy con bug do mình lỡ tay tạo ra chứ không thể thức để đọc mấy cái về DL, mà có đọc thì mình cũng có hiểu đâu 🥲.
- Học lý thuyết quá nhiều mà không đụng tới thực hành, dẫn tới việc bị nản. Khoảng cách giữa lý thuyết và thực hành khá lớn, đặc biệt là với DL. Nếu không thực hành thường xuyên thì tới lúc code model bị yếu đuối đó mọi người. Đừng như mình 🥲.
- DL black box quá. Mình không thích. Mình chả hiểu được mấy cái cơ chế hoạt động của DL. Tại sao khi chỉnh hyperparameters thì model lại tốt hơn hay ngu đi? Chỉ có trời mới biết.
- DL phát triển rất chóng mặt. Vâng đúng vậy, rất chóng mặt:
    - [Highlights of NeurIPS 2023 from Reading All 3584 Abstracts | Alex L. Zhang](https://alexzhang13.github.io/blog/2024/neurips2023/), 3584...
    - ![](/dl/arxiv.png "cs.AI là về AI, còn cs.LG là về Machine learning, và hãy nhìn vào năm 2023 nào mọi người")

    {{< figure align=center src="/stress.jpg" width="200px" caption="stress">}}
    
    Với 1 đứa chậm hiểu như mình thì mình không thể chạy theo tốc độ phát triển của DL được 🥲. Attention, Transformer mình còn chưa hiểu mà Mamba đã đầy rẫy trên cái newsfeed của mình rồi.... Hay khi em Gemini 1.5 của Google vừa được công bố, thì vài tiếng sau đó, OpenAI đã thả Sora ra, cứ như chơi Pokémon vậy.
    
    {{< figure align=center src="/dl/meme.jpg" width="300px" caption="meme nhà làm" >}}

- Resources limitation: Giới hạn về nguồn tài nguyên (GPU), và cả thời gian để đợi con model train xong.
- Về khía cạnh tín hiệu vũ trụ, thì gần đây mình biết được mấy cái này: [mlco2/impact](https://github.com/mlco2/impact), [mlco2/codecarbon](https://github.com/mlco2/codecarbon). Nó cho biết lượng khí thải CO2 khi mình train model có sử dụng GPU ảnh hưởng tới môi trường như thế nào. Một số bài hay hay mà mình đọc được về chủ đề này:
    - https://www.theverge.com/24066646/ai-electricity-energy-watts-generative-consumption
    - https://stanford-cs324.github.io/winter2022/lectures/environment/
    - https://www.forbes.com/sites/robtoews/2020/06/17/deep-learnings-climate-change-problem/
    - https://www.learningtree.com/blog/carbon-footprint-ai-deep-learning/
    - https://news.mit.edu/2020/shrinking-deep-learning-carbon-footprint-0807

    Với 1 đứa toàn train mấy cái linh ta linh tinh trên Colab như mình, mà không thu về được cái gì thì đúng là gây ô nhiễm môi trường thật 🙂.

Rồi giờ sao? Mình không biết, có lẽ là mình sẽ tạm ngưng DL 1 thời gian, hoặc mãi mãi. Tức từ giờ, cuốn Deep Learning của Ian Goodfellow trên máy mình sẽ không còn được mở, hay [Understanding Deep Learning](https://udlbook.github.io/udlbook/), [Dive into Deep learning](https://d2l.ai/) sẽ không còn ở trong cái Onetab của mình nữa. Mình cũng huỷ bớt mấy cái newsletter về DL, sống chậm lại chứ DL vội vã quá 🥲. Có lẽ mình sẽ quay lại nếu bỗng một ngày nào đó thức dậy, mình bỗng hiểu được mấy cái black box của DL, nói chung là vạn sự tuỳ duyên.


Về hướng đi thì chắc là mình sẽ chuyển qua về Machine learning **\\{Deep learning}**, Statistical learning, Optimization, Applied Mathematics, Scientific Computing, hoặc là đá động lại về mảng Data. Ừa, chắc là mình liệt kê hết mấy cái vui vui ngầu ngầu đang có trong đầu của mình rồi.

Vậy mình có hối hận hay có tiếc thời gian dành cho DL không? Câu trả lời là **không**. Dành thời gian khoảng 1 năm để rồi biết mình không hợp với 1 thứ gì đó cũng không hẳn là tốn thời gian đâu. Mà ít ra thì mình còn đọng lại 1 tí về DL để còn ngồi chém gió với mấy đứa bạn của mình.

Bài này hơi suyyy, hứa bài sau sẽ tích cực. Mong rằng học kì này mình vẫn còn sống để còn có bài sau 🥲.

It has been a good game.

Chúc cho Deep learning ngày càng phát triển.

Cheers 🥂.
