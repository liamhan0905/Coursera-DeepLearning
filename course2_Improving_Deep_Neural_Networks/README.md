### Key points from "Initialization" project assignment

- Different initializations lead to different results
- Random initialization is used to break symmetry and make sure different hidden units can learn different things
- Don't intialize to values that are too large
- He initialization works well for networks with ReLU activations.

### Key points from "Regularization" project assignment
- In this assignment I was able to compare the impact of using regularization (3-layer NN with L2-regularization and 3-layer NN with dropout) to fix the overfitting issue. 
- Regularization will help you reduce overfitting.
- Regularization will drive your weights to lower values.
- L2 regularization and Dropout are two very effective regularization techniques.
  #### Key points for drop out
  - Dropout is a regularization technique.
  - You only use dropout during training. Don't use dropout (randomly eliminate nodes) during test time.
  - Apply dropout both during forward and backward propagation.
  - During training time, divide each dropout layer by keep_prob to keep the same expected value for the activations. For example, if keep_prob is 0.5, then we will on average shut down half the nodes, so the output will be scaled by 0.5 since only the remaining half are contributing to the solution. Dividing by 0.5 is equivalent to multiplying by 2. Hence, the output now has the same expected value. You can check that this works even when keep_prob is other values than 0.5.


### Key points from "Gradient Checking" project assignment
- Gradient checking verifies closeness between the gradients from backpropagation and the numerical approximation of the gradient (computed using forward propagation).
- Gradient checking is slow, so we don't run it in every iteration of training. You would usually run it only to make sure your code is correct, then turn it off and use backprop for the actual learning process.