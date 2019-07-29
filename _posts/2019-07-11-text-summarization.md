---
layout : post
title : Text Summarization with Amazon Review Data
---

In this post, we will do automatic summarization using Amazon food reviews.





I used python and tensorflow. The model is **bi-directional RNN and LSTMs** in encoding layer and **attention mechanism** in decoding layer. It is similar to **sequence-to-sequence model** used in [Textsum](https://github.com/tensorflow/models/tree/master/research/textsum).<br>

The title of review is considered as summary and the review is considered as text that I have to summarize. First, I cleaned the raw texts to make it proper for the model. Then I built the model and trained with the training data. After training them, I evaluated the model using pyrouge.<br>

You can see the detail [code](https://github.com/limhyesu98/study_AutomaticSummarization/blob/master/Text_Summarization_with_Amazon_Reviews-version2.ipynb)
and [report](https://github.com/limhyesu98/study_AutomaticSummarization/blob/master/Doc_Text_Summarization_with_Amazon_Review_Data.pdf). The code ipynb file is written in Korean and the report is written in English.
