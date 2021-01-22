### Key points from "Convolution_model_Step_by_Step" project assignment (Week 1)

- Implemented convolutional (CONV) and pooling (POOL) layers in numpy, forward propagation, without using Tensorflow

### Key points from "Convolution_model_Application" project assignment (Week 1)
- Built a model that recognizes SIGN language with almost 80% accuracy on the test set. For this assignment Tensorflow was used.


### Key points from "Keras Tutorial" project assignment (Week 2)
- Used Keras to build a model that recognizes whether a person is smiling or not smiling through images.

### Key points from "Autonomous driving - Car detection" project assignment (Week 3)
- Implemented YOLO algorithm to detect 80 different classes (bus, cars, traffic lights etc) on a video taken when driving.
- YOLO is a state-of-the-art object detection model that is fast and accurate
- It runs an input image through a CNN which outputs a 19x19x5x85 dimensional volume.
The encoding can be seen as a grid where each of the 19x19 cells contains information about 5 boxes.
- Filtered through all the boxes using non-max suppression. Specifically:
	- Score thresholding on the probability of detecting a class to keep only accurate (high probability) boxes
	- Intersection over Union (IoU) thresholding to eliminate overlapping boxes
- Because training a YOLO model from randomly initialized weights is non-trivial and requires a large dataset as well as lot of computation, we used previously trained model parameters in this exercise.


### Key points from "Art_Generation_with_Neural_Style_Transfer_v3a" project assignment (Week 4)
- Applied Neural Style Transfer to generate artistic images.
- Neural Style Transfer is an algorithm that given a content image C and a style image S can generate an artistic image
- It uses representations (hidden layer activations) based on a pretrained ConvNet.
- The content cost function is computed using one hidden layer's activations.
- The style cost function for one layer is computed using the Gram matrix of that layer's activations. The overall style cost function is obtained using several hidden layers.
- Optimizing the total cost function results in synthesizing new images.


### Key points from "Face_Recognition_v3a" project assignment (Week 4)
- Used convnet, specifically faceRecoModel to calculate triple loss as well as use it for face verification and face recognition
- Face verification solves an easier 1:1 matching problem; face recognition addresses a harder 1:K matching problem.
- The triplet loss is an effective loss function for training a neural network to learn an encoding of a face image.
- The same encoding can be used for verification and recognition. Measuring distances between two images' encodings allows you to determine whether they are pictures of the same person.
