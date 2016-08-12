---
style: post
categories: Note
title: Machine Learning Note, P2
---
{% include base.html %}
1. for Normal Equation,feature scaling is not neccessary.

2. the Pro and Cons of using **Gradient Descent** and **Normal Equation**
![gd_vs_ne][pic_1]
But also, GD works on multiple models like classification, while NE only works well on linear regression.

3. causes of (X_t*X) is non-invertible,
  - redundant features, or some dependent features
  - amount of training_set is less than amount of features

4. I'm left to do the last normal equation in proj ex1

[pic_1]: {{base}}/assets/2016-08-09_gd_vs_ne.png
