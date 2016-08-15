---
style: post
categories: Note
title: Machine Learning Note, P4
---
{% include base.html %}

1. Underfitting(high bias), Overfitting(high variance), causes because of too many features

2. Two options in addressing Overfitting,
  - Reduce number of features
  - Regularization

3. Regularized Cost Function for Linear Regression
  ![rcf][regularized_cost_function]

    And should take care on lambda(regularize parameter) choosing, if it's too large it's gonna lead to underfitting

4. Gradient Descent for regularized cost function for linear regression **and logistic regression** is
  ![gd_rcf][gd_rcf_2]

5. Normal Equation with regularization is also available, but I didn't get it.

6. For logistic regression, regularization also applies to Gradient Descent and advanced optimization

7. Andrew smiled: As you've learned Linear/Logistic Regression, Gradient Descent, Advanced optimization and Regularization, you probably know more than quite a lot of engineers working in Silicon Valley who made tons of money. LOLLLL


[regularized_cost_function]: {{base}}/assets/2016-08-15_rcf.png
[gd_rcf_2]: {{base}}/assets/2016-08-15_gd_rcf.png
