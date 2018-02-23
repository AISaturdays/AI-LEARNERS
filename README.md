# AI-LEARNERS
Object detection with Convolutional Neural Network in Keras.

Keras is a Python library for deep learning that wraps the powerful numerical libraries Theano and TensorFlow.
In this, you will find the codes related to object detection with covulational networks using keras. It consist of two codes:

1)Code with a simple convolutional network

2)Code with deeep convolutional network (for better accuracy)

**This includes:

1)  The CIFAR-10 object recognition dataset and how to load and use it in Keras.

2)  How to create a simple Convolutional Neural Network for object recognition.

3)  How to lift performance by creating deeper Convolutional Neural Networks.

**ABOUT THE CIFAR-10 DATASET and HOW TO LOAD IT IN KERAS
  The CIFAR-10 dataset can easily be loaded in Keras.

Keras has the facility to automatically download standard datasets like CIFAR-10 and store them in the ~/.keras/datasets directory using the cifar10.load_data() function. This dataset is large at 163 megabytes, so it may take a few minutes to download.

**SIMPLE CONVOLUTIONAL NETWORK FOR CIFAR-10

We will use a structure with two convolutional layers followed by max pooling and a flattening out of the network to fully connected layers to make predictions.

Our baseline network structure can be summarized as follows:

   1) Convolutional input layer, 32 feature maps with a size of 3×3, a rectifier activation function and a weight constraint of max norm set to 3.
    
  2)  Dropout set to 20%.
    
   3) Convolutional layer, 32 feature maps with a size of 3×3, a rectifier activation function and a weight constraint of max norm set to 3.
    
   4) Max Pool layer with size 2×2.
    
   5) Flatten layer.
    
   6)Fully connected layer with 512 units and a rectifier activation function.
    
   7)Dropout set to 50%.
    
   8)Fully connected output layer with 10 units and a softmax activation function.

**DEEP CONVOLUTIONAL NETWORK FOR CIFAR-10

To improve the accuracy we use deep neural networks. 

We can summarize a new network architecture as follows:

  1)  Convolutional input layer, 32 feature maps with a size of 3×3 and a rectifier activation function.
  
  2) Dropout layer at 20%.
  
  3)  Convolutional layer, 32 feature maps with a size of 3×3 and a rectifier activation function.
  
  4)  Max Pool layer with size 2×2.
  
  5)  Convolutional layer, 64 feature maps with a size of 3×3 and a rectifier activation function.
  
  6)  Dropout layer at 20%.
  
  7)  Convolutional layer, 64 feature maps with a size of 3×3 and a rectifier activation function.
  
  8)  Max Pool layer with size 2×2.
  
  9) Convolutional layer, 128 feature maps with a size of 3×3 and a rectifier activation function.
 10)  Dropout layer at 20%.
 
 11)   Convolutional layer,128 feature maps with a size of 3×3 and a rectifier activation function.
 
 12)   Max Pool layer with size 2×2.
 
 13)   Flatten layer.
 
 14)   Dropout layer at 20%.
 
 15)   Fully connected layer with 1024 units and a rectifier activation function.
 
 16)   Dropout layer at 20%.
 
 17)   Fully connected layer with 512 units and a rectifier activation function.
 
 18)   Dropout layer at 20%.
 
 19)   Fully connected output layer with 10 units and a softmax activation function.

**Extensions To Improve Model Performance

We have achieved good results on this very difficult problem, but we are still a good way from achieving world class results.

Below are some ideas that you can try to extend upon the models and improve model performance.

 1)   Train for More Epochs. Each model was trained for a very small number of epochs, 25. It is common to train large convolutional neural networks for hundreds or thousands of epochs. I would expect that performance gains can be achieved by significantly raising the number of training epochs.
 
  2)  Image Data Augmentation. The objects in the image vary in their position. Another boost in model performance can likely be achieved by using some data augmentation. Methods such as standardization and random shifts and horizontal image flips may be beneficial.
  
  3) Deeper Network Topology. The larger network presented is deep, but larger networks could be designed for the problem. This may involve more feature maps closer to the input and perhaps less aggressive pooling. Additionally, standard convolutional network topologies that have been shown useful may be adopted and evaluated on the problem.
