# Neural Network Charity Analysis

## Overview
The purpose of this analysis is to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. Alphabet Soup’s business team provided a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. WWithin this dataset are a number of columns that capture metadata about each organization, such as the following:

* EIN and NAME—Identification columns
* APPLICATION_TYPE—Alphabet Soup application type
* AFFILIATION—Affiliated sector of industry
* CLASSIFICATION—Government organization classification
* USE_CASE—Use case for funding
* ORGANIZATION—Organization type
* STATUS—Active status
* INCOME_AMT—Income classification
* SPECIAL_CONSIDERATIONS—Special consideration for application
* ASK_AMT—Funding amount requested
* IS_SUCCESSFUL—Was the money used effectively 

## Results
The analysis consisted of two main parts:

*Data Preprocessing*
  * Target variable(s) considered for the model: IS_SUCCESSFUL — 0 and 1 determine if the money was used effectively.
  * Features considered for the model: All other columns, except the target variable, EIN and NAME columns.
  * EIN and NAME columns were neither targets nor features, therefore, removed from the input data.

*Compiling, Training, and Evaluating the Model*
  * The model had three layers:
    1. The first hidden layer had 8 neurons and ReLu activation function.
    2. The second hidden layer had 5 neurons and ReLu activation function as well.
    3. The output layer had 1 neuron and Sigmoid activation function because the probability needed to be predicted as an output. Since probability of successful funding exsist between the range of 0 and 1, sigmoid was the right choice for the output layer.

![model_summary.png](https://github.com/fabeza/Neural_Network_Charity_Analysis/blob/ce9b107c743f35b9bf82733c2ef8d5f68f5af97a/Resources/model_summary.png)

  * Model performance evaluation returned a loss of 0.55 and an accuracy of 72%. The model could be optimized for higher accuracy, the target was to get accuracy above 75%.

![model_accuracy1.png](https://github.com/fabeza/Neural_Network_Charity_Analysis/blob/ce9b107c743f35b9bf82733c2ef8d5f68f5af97a/Resources/model_accuracy1.png)

  * In order to improve model performance, the input data was increased from 403 parameters to 5,421 and the neurons in each hidden layer increased from 8 and 5 to 12 and 4, respectively. After this modifications, the model returned a loss of 0.44 and an acurracy of 79%, an 7% increase from the original model.

![model_accuracy2.png](https://github.com/fabeza/Neural_Network_Charity_Analysis/blob/ce9b107c743f35b9bf82733c2ef8d5f68f5af97a/Resources/model_accuracy2.png)
 
 ## Summary
The original accuracy of 72% was improved to 79% by increasing the input data and neurons in the model. However, better accuracy could be achieved by acquiring more input data, if that is not possible, there are other ways for improving the accuracy of a model including treating missing and outlier values, testing multiple algorithms, and combining the result of multiple weak models and produce better results (ensemble methods). 
