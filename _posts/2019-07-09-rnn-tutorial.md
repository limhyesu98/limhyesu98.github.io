---
layout: post
title: Recurrent Neural Networks Tutorial
---

This post is RNN tutorial written in Korean and it has referenced [WILDML](http://www.wildml.com/2015/09/recurrent-neural-networks-tutorial-part-1-introduction-to-rnns/).





### Part 1: Introduction to RNNS

#### What are RNNs?
Recurrent Neural Network (RNN) 은 sequential inforamtion 을 사용하는 것을 기반으로 한다. 기존의 Neural Network 에서는 모든 input 과 output 이 한 번에 나온다. 그러나 여러 task 에서 이와 같은 방식은 적절하지 않다. RNN 에서 recurrent 는 하나의 sequence 를 이루는 모든 element 에 대해 같은 동작을 반복하기 때문에 붙여진 이름이다. RNN 은 이전에 계산한 정보를 "기억"하고 있다고 볼 수 있다. 이론적으로는 긴 sequence 를 이용할 수 있지만 현실적으로는 한 두 스텝 이전 정보만 이용할 수 있다.  
하나의 단어마다 하나의 층이 존재하는 것처럼 동작하기 때문에 5개의 단어로 구성된 하나의 문장을 예로 들어보자면, RNN 은 5-layer 의 NN 으로 펼쳐지는 것과 같은 동작을 한다. RNN 에서 연산되는 것을 수식화하자면 다음과 같다.  

* $x_t 는 t 시간에 들어온 input 이다. 예를 들어서 $x_1 는 문장에서 두번째 단어에 대한 one-hot vector 일 수 있다.  
* 
