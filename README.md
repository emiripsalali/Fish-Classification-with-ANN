# Fish-Classification-with-ANN

This project aims to develop an artificial neural network (ANN) for image classification. The key components and steps involved in the project are as follows:

Model Architecture:

A sequential model is constructed with the following layers:
An input layer that accepts images flattened into 1D arrays. For instance, an image of size 64x64 pixels with 3 color channels (RGB) will have 12,288 input features (64 * 64 * 3).
One or more hidden layers with a specified number of neurons and activation functions, typically ReLU, to introduce non-linearity.
A dropout layer to reduce overfitting.
An output layer with a softmax activation function, which outputs probabilities for each class in the classification task.
Model Compilation:

The model is compiled using the Adam optimizer and categorical cross-entropy loss function, with accuracy as the performance metric.
Batch Generator:

A batch generator function is implemented to load images and labels in batches. This function normalizes the pixel values to the range [0, 1] before feeding them into the network.
Early Stopping:

An early stopping callback is defined to monitor the validation loss and stop training if there is no improvement for three consecutive epochs, restoring the best weights to avoid overfitting.
Model Training:

The model is trained on training data using the batch generator, with validation data also provided through a separate generator. Training runs for a specified number of epochs, and the steps per epoch are calculated based on the batch size.
Visualization:

After training, the accuracy and loss for both training and validation datasets are visualized using Matplotlib to assess model performance.
Overall, this project demonstrates the process of building, training, and evaluating an ANN for image classification tasks, incorporating techniques to enhance performance and mitigate overfitting.


***KAGGLE NOTEBOOK LINK*** : https://www.kaggle.com/code/emircanipsalali/fish-classification-with-ann-akbank-derin-r?scriptVersionId=203189713
