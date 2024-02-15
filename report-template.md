# Module 12 Report 

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

The purpose of this analysis was to develop supervised machine learning models that can pridt the credit risk. The goal was to leverage dataset of historical lending activity from a peer-to-peer lending services company to create models capable of classifying loans as either healthy  or high-risk of defaulting. By accurately identifying high-risk loans, financial institutions can refine their lending strtegies.

The financial data consists of various variables related to the loans
  * Loan size,
  * Interest rate, 
  * Borrower's income,
  * The debt income ratio,
  * The number of accounts,
  * Derogatory marks against the borrower, and
  * The total debt.

The Loan staus is the target variable denoted by "0" for healthy loans and "1"  for high_risk loans.
The total number of data points are 77536 of which  75036 are healthy loans and 2500 are unhealthy loans. this data set is split into traininag and testing sets. 

The primary machine learning method employed in this analysis was logistic regression.The training set was used to build an initial logistic regression model using the LogisticRegression module from scikit-learn. This model is then applied to the testing data to see if the model can predict the status of loans.

The training data set is resampled with RandomOverSampler module from the Imbalanced-learn. the resampled data is then modeled with Logistic regression ros_classifier. The testing data is used to predict the status of the loan.

## Results


* Machine Learning Model 1(Original data):
  * Balanced accuracy score : 95%
  * precision of predicting healthy loans : 100% recall: 99%
  * precision of predicting hi-risk loans : 85% recall: 91%

* Machine Learning Model 2(Resampled data):
  * Balanced accuracy score : 99%
  * precision of predicting healthy loans : 100% recall: 99%
  * precision of predicting hi-risk loans : 84% recall: 99%
  

## Summary

Based on the results, both Machine Learning Model 1 (trained on original data) and Machine Learning Model 2 (trained on resampled data) have similar precision and recall scores for the healthy loans. The learning model 2 has better recall and f1 score for high-risk loans.This means that Model 2 is more successful in identifying actual high-risk loans correctly, minimizing the risk of missing potentially problematic loans.

Machine Learning Model 2 outperforms Model 1 in terms of balanced accuracy, with a score of 0.99 compared to 0.95. This indicates that Model 2 has a better overall accuracy in predicting both the healthy (0) and high-risk (1) loan labels.

Considering the importance of correctly identifying high-risk loans to manage credit risk effectively, Model 2 is recommended. It achieves a higher overall accuracy and demonstrates better performance in capturing high-risk loans. By using resampling techniques to address the class imbalance, Model 2 has improved its ability to predict high-risk loans accurately.


