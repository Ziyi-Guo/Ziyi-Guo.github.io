---
style: post
categories: Academic
title: Machine Learning Note, P7
---
{% include base.html %}

1. Parameters Unrolling,

    as thetas for every layer in Neuron Network is a matrix, but when we're doing cal in matlab, we have to pass in vectors. We'll need to unroll theta into a long vector

    Reshape the vectors into matrices inside the cost function, to use as theta vectors, easy to cal

2. Gradient Checking.

    Some errors might happen in our implementation of neuron network and lead to disaster,**especially on back propagation**, it's better to have a way to evaluate our gradient calculation.

    Use two-side-epsilon method to calculate the approximation of gradient, use it to compare with the gradient we've got through back_propagation, if they are similar, then we can be sure it's right.

   - implement back propagation to get DVec
   - implement numerical gradient to compute gradApprox
   - Make sure they're similar
   - **turn off gradient checking, use back propagation for training**

   (Be sure to turn gradient checking off before training, or the iteration of numerical gradient computation will be slow)

3. Random initialization,

    **Not put init Theta as all 0, 'cause it's gonna compute all 0s and not update Theta throught iteration**, key is on breaking symmetry

4. Overall note,
    - Pick architecture. Input layer and out put layer are set, the init of hidden layer could be 1, if it doesn't work, put more hidden layers with same units in every hidden layer (better to be more than input features)
    - Train
      + randomly initialize theta
      + implement forward propagation to compute hx
      + implement cost function
      + implement back propagation to get partial derivative
      + run for-loop of forward and back propagation on every input

      + use gradient checking to make sure back propagation works, and turn it off
      + use gradient descent or advanced optimization method with back propagation to minimize cost

5. Stopped implementing back propagation
