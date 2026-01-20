# Neural_network_group_7

## Data:

Obtained from UCI Machine Learning Repository: Concrete Compressive Strength Data Set and used in I-Cheng Yeh, "Modeling of strength of high performance concrete using artificial neural networks," Cement and Concrete Research, Vol. 28, No. 12, pp. 1797-1808 (1998). 

## Problem Statement:
Structural engineers need to know the strength of materials in order to design safe structures. As a machine learning developer working for an engineering company, your job is to analyze data to develop a model that predicts the compressive strength of concrete based on what it is made of and how old the concrete is. The model must also provide an uncertainty in the strength prediction so that engineers can ensure that the design is safe.

## Steps to be completed:
Create a Jupyter notebook and complete the following steps:

### Data

a. Load Concrete_Data_Yeh.csv into a pandas dataframe. Print out the header. Use pandas.DataFrame.describe to summarize the data. Using markdown, explain the meaning of each column and make observations about the dataset.

b. Use pandas.DataFrame.info to check if the entries are the correct datatype, and if there are any missing values. Use pandas.DataFrame.duplicates to check for duplicate entries. Fix the dataset so that there are no missing values, duplicate rows, or incorrect data types. Use markdown to make observations and explain what you have done.

c. Use seaborn.heatmap to display the correlation matrix of the features. Use seaborn.pairplot to generate scatter plots and histograms. Use markdown to make observations and comment on which features are most correlated with compressive strength.
Move the labels to a separate dataframe. Use sklearn.preprocessing.MinMaxScaler to scale the features (but not the labels). Split the data so that 10% is used for testing and 90% for training.

### Modeling (Hint: refer to Exercise 2.02 for help with these steps but note that here we are doing regression while the exercise is on classification, so there are some significant differences.)

a. For both the train and test datasets, save the csMPA column (the label y) as a 2d tensorflow variable and the other columns (the features x) as a separate 2d tensorflow variable. 

b. Use tf.zeros to create tensorflow variables of the appropriate shape for the weights (w) and bias (b).

c. Write a regression function to implement the equation 
 and return the value z. (This is similar to the perceptron function in Exercise 2.02, but without the extra step of using tf.sigmoid. Note that multilinear regression is similar to a perceptron but does not use an activation function.)

d. Write a loss function as a lambda function that calculates 
 where 
 is the label and 
 is the prediction.

e. Write a train function that uses tf.optimizer.SGD to minimize the loss with respect to w and b. Choose an appropriate learning rate. Train a model for at least 1000 epochs on training data.

f. Print out the trained weights and bias. Use the regression function you wrote to predict the strength for each row of training data. Write a function to find the root-mean-squared-error of the predictions and use it to print out the RMSE of the model.

### Conclusion
a. Use your model to make predictions on the test data.

b. Write code to calculate the percentage of deviations 
 that are bigger than the RMSE.

c. Use markdown to comment on how well the model works to make predictions. What uncertainty would you provide to the structural engineers to go along with the strength predictions of the model? 

### Kashish

### Parker

### Hunter

