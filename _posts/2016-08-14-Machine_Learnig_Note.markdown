---
style: post
categories: Academic
title: Machine Learning Note, P3
---
{% include base.html %}

1. Logistic Regression is a CLASSIFICATION algorithm

2. Hypothesis of Logistic regression is like this ![eq][lr_equation]

  while the g(z) is call Sigmoid function

3. Interpretation of hypothesis, h_theta(x) = estimated probability that y = 1 on input x

  h_theta(x) = P(y=1|x;theta)

  so we'll predict y=1 if h_theta(x) >= 0.5 ---that is when theta*x >=0, and predict y=0 if h_theta(x) < 0.5 ---that is when theta*x <0

4. Decision Boundary, the boundary where theta*x==0, since which our hypothesis will predict differently . It's a property of the hypothesis and parameters, not the training set.

5. Separate Cost Function of Logistic Regression
  ![cf][lr_cost_function] the cost will go to infinity when the hypothesis is so wrong from the right answer

6. Overall Cost Function of Logistic Regression
  ![cf_2][lr_cost_function_2]

7. Gradient Descent of Logistic Regression looks just similar to linear Regression, and feature scaling works well in logistic regression as well

8. According to Andrew Ng, it's possible to use complex optimization algorithms without actually understand them. We can use it. Jajaja

9. Multiclass Classification: one-vs-all, take one class(type) data of training set, and use others as antis. So we'll have n classifiers which we'll run each of them and find the one classifier predict max possibility

Stop by 'Solving the problem of Overfitting'

[lr_equation]: {{base}}/assets/2016-08-14 _logistic_regression.png

[lr_cost_function]: {{base}}/assets/2016-08-14_cost_function.png
[lr_cost_function_2]: {{base}}/assets/2016-08-14_cost_function_2.png
