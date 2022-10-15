# Product-Reviews-Classification

The task completed in this project
* create a space distributional semantic representation using tf-idf.
* create a dense distributional semantic representation using Word2Vec 
* Use the better of these approaches to traine and evaluate neural network that can classify an input review to either a positive or a negative class


### Classification Implementation
I have created a Convolutional Neural Network using Keras where the first layer is an
embedding layer that creates a dense vector of the embedding. The next layer is the
Conv1D layer which is a convolutional layer l. The next layer is a GlobalMaxPooling1D layer
which reduces the size of the input. And the final two layers are both dense layers. Finally,
the last layer has a 'sigmoid' activation function as it is suitable for binary classification



### Classification Evaluation and parameters optimization
Neural Networks have a lot of parameters and it is difficult to find all optimal parameters.
I started by finding the best epoch number by just plotting the training accuracies and finding
where the accuracy stops improving and then deciding on epoch number.
Optimizing convolutional layer parameters:
The layer has a lot of parameters. I have used RandomizedSearchCV that tries all
combinations of parameters to find the best parameters for the number of filters and kerne
size and because it takes a lot of time to complete I have tested a small range of
parameters.
And for the classification result, I used 5-fold cross-validation and collected the accuracies
for each run, and then calculated the mean accuracy which equal to 73%
