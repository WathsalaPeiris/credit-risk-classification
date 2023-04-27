# credit-risk-classification
Use of a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* The purpose of this analysis is to train and evaluate a model based on loan risk.
* The data set includes details of loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks and total debt for each record. These varibles are used to predict loan status which is categorised as '1' or '0' where '1' represents a high risk loan and '0' represents a low risk loan.
* The dataset contains total of 77,536 records. Out of these 77,536 records, 75,036 records were identified as low risk and 2,500 records were high risk loans.
* The first step taken in order to build a machine learning model in this analysis was splitting the dataset into trainnig data and testing data using train_test-split method from sklearn.
* Then fitted the trainning data in a logistic regression model (Model 1) and then used that model to predict test data. 
* Following building the first model, the random oversampling method was used to resampling and a new logistics regressin model (Model 2) was created using resampled data set.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  
  * The balanced accuracy score of Model 1 is 0.949 which means only 94.9% of total predictions are correct.
  * Precison score for label '0' is 100% and precision score for label '1' is only 87%. That means almost 100% of all the records that the model has predicted as '0' are actually '0' while out of all the records that the model has predicted as '1', only 87% are actually '1'.
  * Recall score for label '0' is 100% and recall score for label '1' is 90%. That means almost 100% of actual '0's are predicted correctly as '0' and only 90% of actual '1' are correctly predicted as '1'



* Machine Learning Model 2:
  
  * The balanced accuracy score of Model 2 is 0.995 which means only 99.5% of total predictions are correct.
  * Precison score for label '0' is 100% and precision score for label '1' is only 87%. That means almost 100% of all the records that the model has predicted as '0' are actually '0' while out of all the records that the model has predicted as '1', only 87% are actually '1'.
   * Recall score for both labels '0' and '1' are 100% in Model 2 which used resampled trainning set. That means almost 100% of actual '0's  and '1's are predicted correctly as '0' and '1's. 

## Summary

Based on the above two models, the Model 2 performs better than model 1. This is because the accuracy score of model 2 is higher than the accuracy score of Model 1. 
Also the ability to predict actual '1's (high-risk loans) correctly as '1's (high risk loans) is greater than in Model 2 compared to Model 1.

Generally it is good to have high model accuracy, high precision score and high recall score. However, for some datasets, predicting '1's correctly is more important than predicting '0's correctly and for some data sets, it is vice versa. 

In this particular analysis predicting high risk loans ('1') correctly is more important than predicting healthy loans ('0') correctly. This is because the consequences of predicting high risk loan as a healthy loan is more dangerous than predicting a healthy loan as a high risk loan. 
