# Neural Networks for Image Classification

This project consists of testing different neural network architectures and hyperparameters for image classification. The data comes from keras's MNIST dataset of 70,000 digitized handwriting images of numbers from 0-9. 

![](/images/_nn_sample_MNIST_images.png)

The images begin in a 2D array of shape (28, 28) with numbers ranging from 0-255 (0=white and 255=black).

![](/images/_nn_train_images_3.png)

The images are reshaped to 1D of shape (784,) and then rescaled to values between 0-1 by dividing all numbers by 255. Then, one-hot encoding is used to convert the labels from a single 0-9 number to vectors of shape (10,). The training data is split to include 5,000 images and labels for the validation data.

![](/images/_nn_train_labels.png)

## Model Results
Here are the results of 10 different experiments, with different model adjustments as well. The best performing model has a single layer and 512 neurons, with a test accuracy of 98.2% and test loss of 0.102.

![](/images/_nn_models_results.png)

Plotting of the training and validation for loss and accuracy of the top model (512 neurons) and another best-performing model (128):

![](/images/_nn_model_accuracy_loss.png)

## Random Forest
For this experiment, a Random Forest classifier is used to get the relative importance of the 784 features to then select the top 70 features (or pixels). So basically this will take the most important 70 pixels and see how well the model performs. 

![](/images/_nn_rf_heatmap_importance.png)

The model does not perform as well as others, but the 94.6% test accuracy and 0.213 test loss results are still impressive using only 70 pixels as shown below:

![](/images/_nn_rf.png)

