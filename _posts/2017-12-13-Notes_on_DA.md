---
layout: post
title:  "Notes on Domain Adaptation"					# Title of the post
modified: 2017-12-13				# Date
category: Academic
tags: []
comments: true
---
Domain Adaptation论文

- ICML2015, Unsupervised Domain Adaptation by Backpropagation **(DANN)**

    + Learn features that are domain-invariant (domain classifier) and discriminative (label predictor)
    + Introduce a new gate “Gradient Reversal Layer” in applying sgd of adversarial objective (implementation)

    ![DANN_Loss](http://p1k0vaa5f.bkt.clouddn.com/2017-12-13_DANN_loss.tiff)![DANN_net](http://p1k0vaa5f.bkt.clouddn.com/2017-12-13_DANN_net.tiff)


- NIPS2016, Unsupervised Domain Adaptation with Residual Transfer Networks **(RTN)**

  + learn discriminative features via Deep Architectures (CNN), 
  + minimize Maximum Mean Discrepancy(MMD) between source and target domain (Kronecker Product), DL
  + insert residual layers between Source classifier and target classifier, learn permutation function
  + Q: cross-entropy at target classifier

  ![RTN_Loss](http://p1k0vaa5f.bkt.clouddn.com/2017-12-13_RTN_Loss.tiff)


![RTN_Loss](http://p1k0vaa5f.bkt.clouddn.com/2017-12-13_RTN_net.tiff)

- ICML2017, Deep Transfer Learning with Joint Adaptation Networks **(JAN)**

  + Joint Distribution of some untransferable layers are used to minimize the discrepancy of features (JMMD), first model
  + Then add Adversarial scheme in minimizing JMMD (with a network maximizing the JMMD in another dimension)

  ![JAN_Loss](http://p1k0vaa5f.bkt.clouddn.com/2017-12-13_JAN_Loss.tiff)


![JAN_Loss](http://p1k0vaa5f.bkt.clouddn.com/2017-12-13_JAN_net.png)

- NIPS2017, Mean teachers are better role models **(Mean Teacher)**, semi-supervised 
  + Use back-prop to train student as label classifier,
  + Apply Exponential Moving Average (EMA) of network weights as teacher
  + Use mse between predictions of teacher & student as consistency loss
  + Upscaling the unsupervised loss in a time dependent manner is necessary 


![MeanTeacher_Loss](http://p1k0vaa5f.bkt.clouddn.com/2017-12-13_MeanTeacher_Loss.png)![MeanTeacher_net](http://p1k0vaa5f.bkt.clouddn.com/2017-12-13_MeanTeacher_net.tiff)

- arxiv: Self-ensembling for domain adaptation **(Self-Ensembling)** 
  + Applying Mean-Teacher in Domain Adaptation Setting
  + data splited into two paths each iteration: cross-entropy for classification on source-domain & unsupervised self-ensembling loss for target.
  + Two batches — source batch & target batch — were feed each iteration, and different BN parameters are given.
  + SGD is performed jointy![SelfEnsembling_net](http://p1k0vaa5f.bkt.clouddn.com/2017-12-13_SelfEnsembling_net.png)



- ICLR2018: A DIRT-T APPROACH TO UNSUPERVISED DOMAIN ADAPTATION **(Dirt-T)**
  + Unsupervised, non-conservative domain adaptation — a)source fully labeled, target non-labeled; b)classifier works well on both source & target is not guaranteed 

  + introduce clustering assumption on data distribution, applying on a violation term (conditional entropy) in objective function

  + VADA, applying violation penalization for source & target classifier

  + DIRT (Decision Boundary Iterative Refinement) init with VADA, and use violation penalization on target domain to improve the performance on target domain

    ![DirtT_L1](http://p1k0vaa5f.bkt.clouddn.com/2017-12-13_DirtT_L1.png)![DirtT_L2](http://p1k0vaa5f.bkt.clouddn.com/2017-12-13_DirtT_L2.png)

    ![DirtT_L3](http://p1k0vaa5f.bkt.clouddn.com/2017-12-13_DirtT_L3.png)![DirtT_L4](http://p1k0vaa5f.bkt.clouddn.com/2017-12-13_DirtT_L4.png)

    + With Lagrangian multiplier 

  ![DirtT_L5](http://p1k0vaa5f.bkt.clouddn.com/2017-12-13_DirtT_L5.png)



- ICLR2017: Temporal Ensembling for semi-supervised learning **(Temporal Learning)**:
  + Ensemble of NN generally works better than single prediction, more likely to be right.
  + Introducing self-ensembling models , Pi model in taking different translation/noise/dropout paths in extracting same info
  + Temporal ensembling take the Exponential Average Mean of the predictions in past epochs

  ![Temporal_net](http://p1k0vaa5f.bkt.clouddn.com/2017-12-13_Temporal_net.png)

