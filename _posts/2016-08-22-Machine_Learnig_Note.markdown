---
style: post
categories: Note
title: Machine Learning Note, P6
---
{% include base.html %}

1. Neuron Network's Cost Function,
  ![p6_1][neuron_network_cost_functon]


2. Gradient Descent for Neuron Network, **Back Propagation**
  ![p6_2][lower_case_delta]

    delta_up(l)low(j) equals the "error" of the node j in layer l

        delta_up(L) = hx - y;

        delta_up(L-1) = (Theta(L-1))' * delta_up(L) .* g'(z(L-1));

        delta_up(L-2) = (Theta(L-2))' * delta_up(L-1) .* g'(z(L-2));

        ...

        Till delta_up(2) = (Theta(2))' * delta_up(3) .* g'(z(2));

      **Algorithm**
      ![p6_3][back_propagation]

3. Stopped by Unrolling parameters

[neuron_network_cost_functon]: {{base}}/assets/2016-08-22_neuron_network_cost_function.png
[lower_case_delta]: {{base}}/assets/2016-08-22_delta_intuition.png
[back_propagation]: {{base}}/assets/2016-08-22_back_propagation_algorithm.png
