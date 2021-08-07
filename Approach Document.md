# Approach Document

We were provided with dataset of train and test images. The images were loaded using the opencv module and resized to (244,244).
Earlier I tried using a simple CNN model with a few layers which are in the ipynb document name baseline_model which gave an f1 score of only 0.1 approx on the test set.
Therefore I decided to use an existing model from a range of models avavilabe such as MobileNet, Xception in keras.applications. I went ahead first with Xception.
In Xception we did not include the top part and added our own input layer and gave an output layer with softmax activation function with 5 outputs indicating probabilites for each of the classes.
We used a custom callback to print F1 score after each epoch. We then trained the model with only 10 epochs which gave an overall validation F1 Score of 0.9439.
I then tried to run a Resnet101 Model similarly but ran into issues due to unavailability of space on the GPU. Since I had already surpassed the given target, I did not go ahead with any other models
