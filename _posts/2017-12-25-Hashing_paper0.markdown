---
style: post
title: Notes on Hashing 01
---
{% include base.html %}
* ### Supervised Hashing for Image Retrieval via Image Representation Learning([AAAI2014](http://www.iis.sinica.edu.tw/~kevinlin311.tw/cvprw15.pdf "AAAI2017"))
Introducing a Two-Stage learning Scheme.

A Simlarity Matrix $S \in \{-1,1\}^{n\times n}$ is decomposed into $HH^T$ where $H \in \{-1,1\}^{n\times q}$ (Ofc a specific coordinate ascend updating scheme is given, with relaxation that $H \in [-1,1]^{n\times n}$)

![algorithm]({{base}}/assets/2017-12-26_AAAI_1.png)

Then learned codes $H$ is used to guide the learning of deep conv networks (Used [classical Conv_Net in 2012](https://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks.pdf)). Features in last FC layer are used to learn **Binary codes** and **label info** simultaneously.

![stage pic]({{base}}/assets/2017-12-26_AAAI_2.png)

## (最后的分支像不像GAN?)

* ### Simultaneous Feature Learning and Hash Coding with Deep Neural Networks([CVPR2015](http://arxiv.org/pdf/1504.03410v1.pdf "CVPR2015"))

