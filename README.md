## Module 19

# Neural Network Analysis

## Alphabet Soup Charity Neural Network Analysis

## Overview and Objective

In this module I learnt about the neural networks and I am going to use these skills to help the “Alphabet Soup Charity Foundation” to find the right investment opportunities. With the application of machine learning and neural networks on the dataset  provided, I developed a classifier model that can predict if the applicants will be successful for not if funded by the Alhabet Soup.
In this module I used the following resources:

•	Scikit-Learn

•	Pandas

•	TensorFlow

•	Keras

## Data Preprocessing

•	First, I downloaded the data and dropped the column “Name”.

•	Then I checked the unique number of items in each column of the dataset and found out that the columns  “Application Type” and “Classification” could be binned.

•	I found out the count of types of items for both of the columns and plotted its density curve.

•	In “Application_Type” column where the number of counts for the items are less than 200 were binned in the “other” category. Similarly, in column “Classificatio_count” if the number of counts for the items are less than 800 then they are binned in the “Others” category.

•	Then I found out the columns (“Application_Cat”) which are strig datatypes and encoded then into numerical values as machine learning only accepts the numerical values. 

•	Then we assigned the target and features arrays to its respective variables and performed the splitting of the preprocessed data in to training and testing datasets.


## Compile, Train and Evaluate the Model

•	I defined the input features and hidden nodes for each hidden layers for deep neural network model. 

•	I defined checkpoint path and the filenames.

•	Complied the model with loss as binary_crossentropy and optimizer as “adam”.

•	Created a callback which saves the model’s weight every 5 epochs.

•	Then evaluated the model using test data and exported to HDF5 file so that anyone can use it later.


## Results:

•	In the first attempt I kept 8 neurons in the first layer and 6 neurons in the second layer. Both had relu activation functions, which was giving me the following a loss and accuracy:


268/268 - 0s - loss: 0.5544 - accuracy: 0.7273 - 303ms/epoch - 1ms/step Loss: 0.5544235110282898, Accuracy: 0.7273469567298889

•	In the second attempt I changed the hidden nodes in first layer to 24 and second layer to 12 nodes, which gave the loss and accuracy as follows:
268/268 - 1s - loss: 0.5542 - accuracy: 0.7257 - 666ms/epoch - 2ms/step
Loss: 0.5541909337043762, Accuracy: 0.7257142663002014

•	In the third attempt, I dropped a column “Special_considerations”, which did not made any changes in the loss and the accuracy:


268/268 - 1s - loss: 0.5542 - accuracy: 0.7257 - 666ms/epoch - 2ms/step
Loss: 0.5541909337043762, Accuracy: 0.7257142663002014

•	In fourth attempt, I changed the activation function of the second layer to “tanh” and gave the following loss and accuracy:

268/268 - 0s - loss: 0.5523 - accuracy: 0.7275 - 312ms/epoch - 1ms/step Loss: 0.5523343682289124, Accuracy: 0.7274635434150696


## Summary

I made four attempts to improve the accuracy of the model but with all the attempts there was not any significant improvement in the accuracy of the model. There could be many more options which I could have tried to improve the accuracy but due to the limited amount of time I stopped attempting and could not improve the accuracy to 75%. 
