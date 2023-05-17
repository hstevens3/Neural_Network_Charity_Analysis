# Module 20 Challenge Neural Network Model

# Neural_Network_Charity_Analysis

## Overview of Project

Using the starter code provided, this challenge is to create a neural network model to predict which non-profit organizations will successfully use the funding. The model will be developed on a large dataset with features and a target variable. 

## Results

### Data Preprocessing

The target variable is IS_SUCCESSFUL. The identification columns EIN and NAME are not used in the analysis. I also removed STATUS and SPECIAL_CONSIDERATIONS when optimizing the model. The rest of the variables are features in the model. The categorical variables were binned when few values were present. And the data was scaled.

### Compiling, Training, and Evaluating the Model

I selected 80 neurons for the first layer, as that is double the number of columns.  for the second layer I tried 30 and 50, both had similar accuracy results. When optimizing, I tried adding a third layer, increased the epochs to 1000 and binned the ASK AMT. Nothing made much difference in the accuracy. I used relu and sigmoid for the activation functions since it was a binary classification. I was not able to achieve greater than 75% accuracy.


## Summary

- The 72% accuracy for the model is only fair. If I was doing this outside of a learning environment, I would look for more context on the data. For example, most of the ASK AMT were 5000 and there were some extreme outliers. Maybe that column could be dropped from the analysis. Also, the keras tuner could be used to give the best performance, but with 80 neurons I wasn't sure if running that would be very resource intensive so I did not run it.