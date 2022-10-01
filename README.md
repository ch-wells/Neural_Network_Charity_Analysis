# Neural_Network_Charity_Analysis

## Overview of the analysis
The purpose of this project was to determine which applications for nonprofit support were most promising based on the previous performance of grantees.

## Results 

### Data Preprocessing
- The target variable is IS_SUCCESSFUL
- The features include APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS and ASK_AMT      
- The variables EIN and NAME have been removed from the data set

## Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
Initially, I started with 2 hidden layers with 80 and 40 neurons each.  I selected 80 neurons because it is roughly twice the number of features to be processed.

- Were you able to achieve the target model performance?
The first run did not achieve target performance, achieving only .43 accuracy.  

- What steps did you take to try and increase model performance?
In subsequent attempts, I removed STATUS from the initial data pool, rebinned the categorical variables, and raised the total epochs to 200.  This brought the accuracy to .53.  For the next attempt, I added an additional hidden layer with 20 neurons and kept the total epochs at 200 and this kept the accuracy at .59.  Next I swapped out ReLu for Sigmoid, but that also returned .53. 

### Summary 
I did not reach the target of .75 over the course of three attempts.  The most successful attempt had three hidden layers and 200 epochs.  Future attempts might include adding additional hidden layers with additional neurons and epochs.  I could also reexamine the features included and the binning choices made.  Given that this is a binary classification problem, we could also try other supervised models, like logistic regression or random forest.