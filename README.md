# Image-Classification
## Project goal
The goal of this project is to train and test a neural network that performs image classification. The neural network will predict whether an image is an airplane, a bird, or an automobile.

## Steps taken to analyze the data
1. I used Keras Tuner to find the best model architecture. I used 10 epochs. I conducted a parameter sweep using the following parameter values:
    - Units per layer: 512 or 3072
    - Number of layers: 2, 3, 4, or 5
    - Activation function: sigmoid or ReLU
    - Learning rate: logarithmically spaced values between 1^(-5) and 1^(-1)
    - L2 regularization coefficient: logarithmically spaced values between 1^(-5) and 1^(-1).
2. The best model architecture had 512 units per layer, a sigmoid activation function, 4 layers, a learning rate of about 0.00029, and an L2 regularization coefficient of about 0.00017. I loaded that model in. (Note that all the layers had the same number of units and the same activation function except the output layer, which had 3 units and a softmax activation function).
3. I used that model to make a prediction on the test dataset. I calculated the accuracy and printed out the confusion matrix. The accuracy was 76.7%.
4. I calculated the percentage of test examples in each class that were classified correctly. For birds, this was 78.2%. For planes, it was 78.3%. For automobiles, it was 73.6%.
5. I looked at some of the misclassified images to see if they were blurry and hard to classify for a human or if the misclassification was due to the neural network.

## File that performs the data analysis
The file that performs the data analysis steps is David_Stanko_image_classification.ipynb.
