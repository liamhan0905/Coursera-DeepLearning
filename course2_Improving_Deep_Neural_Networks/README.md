### Key points from "Initialization" project assignment (Week 1)

- Different initializations lead to different results
- Random initialization is used to break symmetry and make sure different hidden units can learn different things
- Don't intialize to values that are too large
- He initialization works well for networks with ReLU activations.

### Key points from "Regularization" project assignment (Week 1)
- In this assignment I was able to compare the impact of using regularization (3-layer NN with L2-regularization and 3-layer NN with dropout) to fix the overfitting issue. 
- Regularization will help you reduce overfitting.
- Regularization will drive your weights to lower values.
- L2 regularization and Dropout are two very effective regularization techniques.
  #### Key points for drop out
  - Dropout is a regularization technique.
  - You only use dropout during training. Don't use dropout (randomly eliminate nodes) during test time.
  - Apply dropout both during forward and backward propagation.
  - During training time, divide each dropout layer by keep_prob to keep the same expected value for the activations. For example, if keep_prob is 0.5, then we will on average shut down half the nodes, so the output will be scaled by 0.5 since only the remaining half are contributing to the solution. Dividing by 0.5 is equivalent to multiplying by 2. Hence, the output now has the same expected value. You can check that this works even when keep_prob is other values than 0.5.


### Key points from "Gradient Checking" project assignment (Week 1)
- Gradient checking verifies closeness between the gradients from backpropagation and the numerical approximation of the gradient (computed using forward propagation).
- Gradient checking is slow, so we don't run it in every iteration of training. You would usually run it only to make sure your code is correct, then turn it off and use backprop for the actual learning process.

### Key points from "Optimization Methods" project assignment (Week 2)
- The difference between gradient descent, mini-batch gradient descent and stochastic gradient descent is the number of examples you use to perform one update step.
- You have to tune a learning rate hyperparameter α.
- With a well-turned mini-batch size, usually it outperforms either gradient descent or stochastic gradient descent (particularly when the training set is large).
- Shuffling and Partitioning are the two steps required to build mini-batches
- Powers of two are often chosen to be the mini-batch size, e.g., 16, 32, 64, 128.
- Momentum takes past gradients into account to smooth out the steps of gradient descent. It can be applied with batch gradient descent, mini-batch gradient descent or stochastic gradient descent.
- You have to tune a momentum hyperparameter  ββ  and a learning rate  αα .
- Some advantages of Adam include:
  - Relatively low memory requirements (though higher than gradient descent and gradient descent with momentum)
  - Usually works well even with little tuning of hyperparameters (except  αα )

  ### Key points from "Tensorflow Tutorial" project assignment (Week 3)
- Create placeholders
- Specify the computation graph corresponding to operations you want to compute
- Create the session
- Run the session, using a feed dictionary if necessary to specify placeholder variables' values.
- Built neural network in tensorflow capable of recognizing an image with high accuracy(SIGNS dataset)
- Tensorflow is a programming framework used in deep learning
- The two main object classes in tensorflow are Tensors and Operators.
- When you code in tensorflow you have to take the following steps:
  - Create a graph containing Tensors (Variables, Placeholders ...) and Operations (tf.matmul, tf.add, ...)
  - Create a session
  - Initialize the session
  - Run the session to execute the graph
- You can execute the graph multiple times as you've seen in model()
- The backpropagation and optimization is automatically done when running the session on the "optimizer" object.