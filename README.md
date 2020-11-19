# Neural Network Charity Analysis

## Overview
Alphabet Soup is a non-profit philanthropic foundation dedicated to helping organizations that protect the environment, improve people’s wellbeing, and unify the world. Unfortunately, not every donation the company makes is impactful. They are looking to predict which organizations are worth donating to and which are too high risk. To find out whether applicants will be successful if funded by them, we will design and train a deep learning neural network model that will evaluate all types of input data and produce a clear decision-making result. This model will help Alphabet Soup determine which organizations should receive donations.

## Results
### *Data Preprocessing*
**Target variable**
  -	The variable `IS_SUCCESSFUL` was considered as the target for this model.
  
**Feature variables**
  -	The variables `APPLICATION_TYPE`, `AFFILIATION`, `CLASSIFICATION`, `USE_CASE`, `ORGANIZATION`, `STATUS`, `INCOME_AMT`, `SPECIAL_CONSIDERATIONS`, and `ASK_AMT` were considered to be the features for this model.

**Non-target/features**
  -	The variables `EIN` and `NAME` were neither targets nor features, and were removed from the input data.


### *Compiling, Training, and Evaluating the Model*
1. These were the neurons, layers, and activation functions selected for the neural network model:  
  - Hidden layer 1 = 80 neurons, Activation = ReLU  
  - Hidden layer 2 = 30 neurons, Activation = ReLU  
  - Output layer Activation = Sigmoid  

2. I was not able to achieve the target model performance of 75%. The initial model was only able to achieve an accuracy of 72.54%.

3. These were the steps taken to try and increase the model performance:
  - Dropped the `ASK_AMT` column, in addition to the `EIN` and `NAME` columns
  -	Decreased the binning value counts size for the `APPLICATION_TYPE` column from 1,000 to 500
  -	Decreased the binning value counts size for the `CLASSIFICATION` column from 2,000 to 1,500
  -	Increased the number of nodes from 80 to 126 in the first hidden layer
  -	Increased the number of nodes from 30 to 126 in the second hidden layer
  -	Increased the number of epochs from 50 to 100

## Summary
Even after executing the steps above to try and increase model performance, I was not able to get it to reach an accuracy of 75%. However, I was able to increase the model performance by 0.53% from 72.54% to 73.07%. 

### Recommendation
A balanced random forest classifier could potentially solve this classification problem. I recommend this model for its speed and ease of implementation. This model is capable of training on large datasets and predicting values in seconds, compared to the deep learning model which require several minutes. Because this model is faster and easier to implement than a deep learning neural network, the company would be saving time and resources, which I believe would be worth it, considering both models’ predictive accuracies being very similar.
