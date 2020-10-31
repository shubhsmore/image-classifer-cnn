# image-classifer-cnn

This project is made as Test for Internship with [IotIot](http://iotiot.in/) \
</br>
In this I have created Image classification using convolutional neural network. \
</br>
I used the pre-built dataset of images i.e fashion MNIST. You can directly import Fashion MNIST from TensorFlow.  
</br>
- First we'll import the libraries we need,  
```
import tensorflow as tf
import numpy as np
import matplotlib.pyplot as plt
```  
</br>
- Then we import the Fashion MNIST Dataset.
</br>
- We just explore the dataset now.
  1. Length of training data
  2. Length of testing data
  3. Shape
  </br>
- If you inspect the first image in the training set, you will see that the pixel values fall in the range of 0 to 255. \
Scale these values to a range of 0 to 1 before feeding them to the neural network model. To do so, divide the values by 255.
</br>
- Now we'll build the model
  1. The first layer in this network, ```tf.keras.layers.Flatten```, transforms the format of the images from a two-dimensional array (of 28 by 28 pixels) to a one-dimensional array (of 28 * 28 = 784 pixels).
  2. After the pixels are flattened, the network consists of a sequence of two ```tf.keras.layers.Dense layers```. These are densely connected, or fully connected, neural layers. 
  3 .The first Dense layer has 128 nodes (or neurons). The second (and last) layer returns a logits array with length of 10. 
</br>
- Lets Compile the model \
Before the model is ready for training, it needs a few more settings. These are added during the model's compile step:  
  1. Loss function —This measures how accurate the model is during training. You want to minimize this function to "steer" the model in the right direction.
  2. Optimizer —This is how the model is updated based on the data it sees and its loss function.
  3. Metrics —Used to monitor the training and testing steps. The following example uses accuracy, the fraction of the images that are correctly classified.
</br>
- Train The model 
  1. Feed the training data to the model. In this example, the training data is in the train_images and train_labels arrays.
  2. The model learns to associate images and labels.
  3. You ask the model to make predictions about a test set—in this example, the test_images array.
  4. Verify that the predictions match the labels from the test_labels array.
</br>
- To start training, call the model.fit method 
</br>
- Next, we'll compare how the model performs on the test dataset
</br>
- With the model trained, you can use it to make predictions about some images. The model's linear outputs, logits. Attach a softmax layer to convert the logits to probabilities, which are easier to interpret.
