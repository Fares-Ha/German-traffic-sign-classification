# German-traffic-sign-classification
In this project I create a Deep learning model for traffic signs classification an I got 97.78% accuracy on test dataset

## First I did Data preprocessing :

1- edit the input shape

2- convert target to onehot encoding

3- convert input from RGB to Grayscale

4- standardize the input ( mean = 0 , std = 1 )

## Then I create the sequential model using Keras, the model Architecture is:

Convolutional layer (32, (3,3), activation = 'relu', input_shape = (32, 32,1)))

Batch Normalization layer

AveragePooling layer (2,2)

Dropout layer (0.27)

Convolutional layer (64, (3,3), activation = 'relu', input_shape = (32, 32,1)))

Batch Normalization layer

AveragePooling layer (2,2)

Dropout layer (0.27)

Convolutional layer (128, (3,3), activation = 'relu', input_shape = (32, 32,1)))

Batch Normalization layer

AveragePooling layer (2,2)

Dropout layer (0.27)

Flatten layer

Dense layer (120, activation = 'relu')

Batch Normalization layer

Dropout layer (0.27)

Dense layer (64, activation = 'relu')

Batch Normalization layer

Dropout layer (0.27)

Dense layer (43, activation = 'softmax')

## Finally I trained the model

I used Adam as an optimizer, categorical_crossentropy as a loss function, and accuracy as a metric

I tarined the model for 50 epochs and batch size = 50
