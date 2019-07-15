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

