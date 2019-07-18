---
layout : post
title : Summarization with Pointer-Generator Networks
---

This post is a reveiw of this ACL 2017 [paper](https://arxiv.org/abs/1704.04368)
*Get To The Point: Summarization with Pointer-Generator Networks* by See et al.<br>





There are two types of automatic summarization : extractive and abstractive.
Extractive summarization is much easier to implement but abstractive one is much more
 powerful and human-friendly.<br>
 
Neural sequence-to-sequence models have improved abstractive text summarization.
But there are still few big problems, so by using Pointer-Generator Networks and coverage,
the author tried to solve those problems and ended up with huge improvements.<br>

#### Basic Recurrent Neural Networks
First, let's look at the basic Recurrent Neural Networks(RNNs). It is constructed with bidirectional encoder RNN, uni-directional decoder RNN, attention distribution, context vector, and vocabulary distribution.<br>

1. Encoder RNN reads the source text word-by-word and produce the encoder hidden states. <br>
2. After the encoder reads the whole source text, the decoder RNN starts to produce the output which forms the summary. The decoder RNN recieves previous deocer output as input and produces the **decoder hidden states**. <br>
3. The hidden state is used to calculate the **attention distribution**. Attention distribution is the probability distribution over the words in the source text and this tells the decoder where to look to produce the next word.<br>
4. The attention distribution is used to calculate the **context vector**. The context vector is a weighted sum of the encoder hidden states and the weight is attention distribution for each step.<br>
5. At the last, context vector and decoder hidden state are used to calculate **vocabulary distribution**. The vocabulary distribution is the final result of this model that is a probability distribution over all the words in a large fixed vocabulary. This is the final distribution from which to predict the word. The word with the largest probability is chosen as output.<br>

In this way, RNN with attentional mechanism creates summary from reading the source text.

#### Two Big Problems in RNN
There are two big problems in this approach.

1. The model makes **factual errors**, a nonsensical sentence and cannot handle OOV(Out-Of-Vocabulary) words.
2. The summary sometimes **repeats itself**.

The causation of the first problem is that sequence-to-sequence-with-attention model makes it too difficult to copy a word from the source text. In order to copy a word from the source, the word has to pass through several layers of computation so that it is not easy to recover.<br>

The second problem, repetition is caused by decoder's over-reliance on the decoder output. Decoder takes its previous output as input. Therefore, single repeated triggers an endless repetitive cycle.

#### Easier Copying with Pointer-Generator Networks
**Pointer-generator network** is the solution for the first problem(creating factual errors).


#### Reference
[Blog post](http://www.abigailsee.com/2017/04/16/taming-rnns-for-better-summarization.html) written by Abigail See, the author of the paper.
