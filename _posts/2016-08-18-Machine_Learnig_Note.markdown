---
style: post
categories: Academic
title: Machine Learning Note, P5
---
{% include base.html %}

1. Neuron Networks, it's origin were trails trying to mimic brain.

2. One learning algorithm Hypothesis, as given certain input to a part of brain, it can learn how to deal with different inputs

3. See neuron as a logistic unit like this
  ![p1][logistic_unit]

    and the network diagram is like this
  ![p2][neuron_network]
  1st layer is called *input layer*, last layer is called *output layer*, while the layers in between are called *hidden layer*

4. Notations and Calculation.
  - notation of value
    ![p3][activation_notation]
  - notation of theta
    ![p4][theta_notation]
  - Calculation of Neuron network
    ![p5][calculation]
  - Size of theta per layer
    ![p6][size_of_theta]

5. Forward Propagation
  is quite like a vectorized way of calculating the neuron network.
  ![p7][forward_propagation]

6. Neuron Network is **learning it's own features**

7. Multiple Classification, just like one-vs-all

8. Stop by matlab training with neuron network.



[logistic_unit]: {{base}}/assets/2016-08-18_logistic_unit.png
[neuron_network]: {{base}}/assets/2016-08-18_network.png
[activation_notation]: {{base}}/assets/2016-08-18_activation_notation.png
[theta_notation]: {{base}}/assets/2016-08-18_theta_notation.png
[calculation]: {{base}}/assets/2016-08-18_calculation.png
[size_of_theta]: {{base}}/assets/2016-08-18_size_of_theta.png
[forward_propagation]: {{base}}/assets/2016-08-18_forward_propagation.png
