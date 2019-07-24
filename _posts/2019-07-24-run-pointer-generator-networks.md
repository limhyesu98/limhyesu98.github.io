---
layout : post
title : Running the Code for Pointer-Generator Networks
---

In this post, tutorial for running the code and the result of running is written.




Since I am using Python3 with Tensorflow 1.0, I followed this [code](https://github.com/becxer/pointer-generator/). This code was similar to [TextSum code](https://github.com/limhyesu98/models/tree/master/research/textsum), which I have done research [here](https://github.com/limhyesu98/myTextSum).<br>

### Getting the dataset
This model used CNN/Daily Mail dataset which has multi-sentence summary. Following the instructions from [here](https://github.com/abisee/cnn-dailymail), I have got some chunked datafiles.<br>

### Training and Evaluating
I have trained this model for 24h.

### Beam Search Decoding
I have done the decode job and visualized by following this [instruction](https://github.com/abisee/attn_vis).
Also I got the ROUGE score using pyrouge. The result is as below.<br>
#### ROUGE-1:
rouge_1_f_score: 0.3016 with confidence interval (0.2995, 0.3036)<br>
rouge_1_recall: 0.3140 with confidence interval (0.3116, 0.3162)<br>
rouge_1_precision: 0.3175 with confidence interval (0.3150, 0.3200)<br>

#### ROUGE-2:
rouge_2_f_score: 0.1194 with confidence interval (0.1176, 0.1209)<br>
rouge_2_recall: 0.1251 with confidence interval (0.1232, 0.1268)<br>
rouge_2_precision: 0.1256 with confidence interval (0.1237, 0.1273)<br>

#### ROUGE-l:
rouge_l_f_score: 0.2717 with confidence interval (0.2697, 0.2736)<br>
rouge_l_recall: 0.2831 with confidence interval (0.2809, 0.2851)<br>
rouge_l_precision: 0.2861 with confidence interval (0.2837, 0.2884)<br>

The ROUGE scores were lower than scores from the paper. Parameters such as ***max_enc_steps*** or ***max_dec_steps*** may have impact on it. 
