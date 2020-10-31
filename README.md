# image-classifer-cnn

This project is made as Test for Internship with [IotIot](http://iotiot.in/) \
In this I have created Image classification using convolutional neural network. \
I used the pre-built dataset of images i.e fashion MNIST. You can directly import Fashion MNIST from TensorFlow.  
  
- First we'll import the libraries we need,  
```
import tensorflow as tf
import numpy as np
import matplotlib.pyplot as plt]
```  
- Then we import the Fashion MNIST Dataset 
- We just expore the dataset 
  1. Length of training data
  2. Length of testing data
  3. Shape
- If you inspect the first image in the training set, you will see that the pixel values fall in the range of 0 to 255. \
Scale these values to a range of 0 to 1 before feeding them to the neural network model. To do so, divide the values by 255.
- Now we'll build the model
The first layer in this network, tf.keras.layers.Flatten, transforms the format of the images from a two-dimensional array (of 28 by 28 pixels) to a one-dimensional array (of 28 * 28 = 784 pixels). \
After the pixels are flattened, the network consists of a sequence of two tf.keras.layers.Dense layers. These are densely connected, or fully connected, neural layers. The first Dense layer has 128 nodes (or neurons). The second (and last) layer returns a logits array with length of 10. \


