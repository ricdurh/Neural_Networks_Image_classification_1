# Neural Networks for Image Classification

This project consists of testing different neural network architectures and hyperparameters for image classification. The data comes from keras's MNIST dataset of 70,000 digitized handwriting images of numbers from 0-9. 

![](/images/_nn_sample_MNIST_images.png)

The images begin in a 2D array of shape (28, 28) with numbers ranging from 0-255 (0=white and 255=black).

![](/images/_nn_train_images_3.png)

The images are reshaped to 1D of shape (784,) and then rescaled to values between 0-1 by dividing all numbers by 255. Then, one-hot encoding is used to convert the labels from a single 0-9 number to vectors of shape (10,). The training data is split to include 5,000 images and labels for the validation data.

![](/images/_nn_train_labels.png)

