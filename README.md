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
- Then we import the Fashion MNIST Dataset \
- We just expore the dataset \
  1. Length of training data
  2. Length of testing data
  3. Shape
- If you inspect the first image in the training set, you will see that the pixel values fall in the range of 0 to 255. Scale these values to a range of 0 to 1 before feeding them to the neural network model. To do so, divide the values by 255.


