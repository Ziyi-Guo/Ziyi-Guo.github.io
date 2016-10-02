---
style: post
categories: Note
title: Machine Learning Note, P8
---
{% include base.html %}

1. Machine Learning diagnostic: a test that you can run to gain insight what is/isn't working with a learning algorithm and gain guidance on how best to improve the performance

2. Evaluating the hypothesis

    - Cross validation. Divide the data set into two parts: **Training Set(70%) and Test Set(30%)**. Learn the parameters from the training set and implement them on test set, find out the errors. Choose the model with least test error

3. As the learning algorithm will work well on dataset we got, the error of the model we choose on test set, is likely to be more optimistic than the generalized error. So one step further than 2, we divide dataset into 3 parts : **Training Set(60%), Cross validation Set(20%), test set(20%)**
  ![p1][errors]

  After train the model with training set, estimate the errors with the cross validation set, choose the model with best cross validation set, then estimate the generalized error on test set



[errors]: {{base}}/assets/2016-09-19_Cross_Validation_Errors.png
