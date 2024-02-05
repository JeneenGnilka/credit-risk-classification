# Module 12 Report Template

## Overview of the Analysis


The purpose of this analysis is to train and evaluate a model based on loan risk.  that could predict the creditworthiness of borrowers. 
The financial information contained metrics related to individual borrowers including loan size, Interest Rate, Borrower Income, Debt to 
Income Ratio, Number of Accounts, Derogatory Marks, Total Debt, and Loan Status. 

The model was to predict Loan Status based on Interest Rate, Borrower Income, Debt to Income Ratio, Number of Accounts, Derogatory Marks, 
and Total Debt. The data included 75,036 healthy loans and 2,500 high-risk loans.

After importing data from the CSV, I created the labels set from the "loan_status" column and created the features using the remaining columns. 

Machine leaning process
  Checked the balance of the labels variable using the value_counts function
  Split the data into training and testing datasets using train_test_split
  Fit the model using the training data
  Saved predictions based on test data and fitted the model
  Evalueated the models performance using balanced_accuracy_score, a confusion matrix, and a classification repot

I used the Logistic Regression Model using the original data and also used the Logistic Regression Model using RandomOverSampler. RandomOverSampler 
helps to address the class imbalance in the loan_status variable.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1: Logistic Regression Model with Original Data
  * Balanced Accuracy Score: 0.967989851522121
  * Precision: Healthy Loans 1.00, High-Risk Loans 0.84
  * Recall: Healthy Loans 0.99, High-Risk Loans 0.94
  * F1-Score: Healthy Loans 1.00, High-Risk Loans 0.89


* Machine Learning Model 2: Logistic Regression Model with Resampled Training Data
  * Balanced Accuracy Score: 0..993624830883812
  * Precision: Healthy Loans 1.00, High-Risk Loans 0.84
  * Recall: Healthy Loans 0.99, High-Risk Loans 0.99
  * F1-Score: Healthy Loans 1.00, High-Risk Loans 0.91


## Summary

The Logistic Regression Model with Original Data is very effective at classifying Healthy Loans. It also does reasonably well at predicting High-Risk Loans, 
though the precision, recall and F1-score are lower than that of the Healthy Loans.

The Logistic Regression Model with Resampled Training Data is very effective at predicting both Healthy Loans and High-Risk Loans.

Though both models do equally well in predicting Healthy Loans, the second machine learning model using resampled training data is better able to predict High-Risk Loans. 

I would recommend the Logistic Regression Model with Resampled Training Data due to it being better able to predict High-Risk Loans.

