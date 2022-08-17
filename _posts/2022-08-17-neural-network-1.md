---
layout: post
title:  Neural Networks (1)
date:   2022-8-17
author: Yechengnuo Zhang
---

## Introduction

人工智能的应用就不多说了。神经网络属于人工智能的一种，大的分类可以概括成：人工智能 包含 机器学习 包含 神经网络。神经网络的算法就是模仿人脑的神经元和突触进行工作的。神经元(Neuron)之间由突触(Synapses)进行信息传递。神经网络的基本结构也是如此。

<div  align="center"><img src="/assets/images/posts/20220817/neuron.jpg"/></div>

如上图，其实基本结构非常清晰明了。如果学过一些电路，这东西简单来说就是一个加法器和乘法器的组合体，数据进去，加起来，再给到一个函数里面，然后输出。下面会更详细地说neuron的工作原理，这里随便看看就行。

## Neuron Scheme

每个neuron都是一个信息处理单元。一个典型neuron的结构如下图所示：

<div  align="center"><img src="/assets/images/posts/20220817/neuron_scheme.jpg"/></div>

如图，一个neuron基本包含以下元素：

1. A set of synapses or connections.一组突触的input集。每一个input会和这条突触上面的权重(weight)相乘。

2. A bias.一个偏置，这个偏置可以把它当成是一个input一直为1的weight，在代数表达里面就是和input的0次方相乘。

3. An adder.一个加法器，把刚才和weight相乘的input全部加起来。这里加完之后输出结果是v,英文里一般叫这个v是local field。

3. 