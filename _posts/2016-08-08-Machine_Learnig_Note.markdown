---
style: post
categories: Academic
title: Machine Learning Note, P1
---
{% include base.html %}

1. Linear Regression, Hypothesis, cost function, Gradient Descent

2. For multiple features linear regression, feature scaling helps to make converge faster,
get every feature into approximately a -1<= x(i) <= 1 range or *mean normalization*
( x[i] - x_mean) / (x_max - x_min)

3. To make sure Gradient Descent work, can run the gradient descent for 100 or some iterations, plot
J(theta), the slope should decrease after every iteration.
Or could declear convergence if J(theta) decrease less than a very small value in one iteration.
**sufficiently small alpha, J(theta) should decrease on every iteration, but if alpha is too small, would be slow to converge**,might try alpha (learning rate) with 1/100 to 10

4. Mind the choice of features, polynomial function

5. Normal Equation, a way to solve the problem analytically   
 ![pic][n_equation]



[n_equation]: {{base}}/assets/normal_equation.png
