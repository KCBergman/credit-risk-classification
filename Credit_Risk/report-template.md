# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

The purpose of this analysis was to use machine learning to predict which loans are at risk of defaulting, out of a group of loans. This could be something that a bank might use when analyzing the loans they've made to different customers. A bank could use this model to determine which of their customers they should give extend credit to -- knowing that the bank does not want to give loans to people likely to default on the loan.

The data used in this model was historical loan data for a large group of customers. Each row of data was specific to a loan, and included loan size, interest rate, the borrower's income, the debt to income ratio of the borrower, the number of accounts the borrower held, derogatory marks, total debt held by a borrower, and whether the loan was healthy or at high risk of defaulting. 

The model is trying to predict the loan status -- whether or not a loan is healthy or at high risk of defaulting. The dataset used to build the model contained 77,536 loans total (rows). 2500 of the loans had a loan status of high risk for defaulting. Using the other variables (income, debt to income ratio, number of accounts, etc.) the model was trying to predict what the outcome would be in the column for loan status. 

The first step in the process was calling the csv file in and creating a dataframe to hold the information about each loan. From there I separated the target (loan status) values as a variable (y) and had the rest of the dataframe (the inputs) saved as another variable (X). I checked the balance of the y variable by using the value counts function and then I used the train-test-split function to separate the data into two groups -- training data and testing data. There was an X-train set of data, an x-test set of data, a y-train set of data, and a y-test set of data. I used a logistic regression method from Scikit Learn and fit it to the training data (X and y). Then I saved predictions using the regression model and compared the predictions to the data in the testing set of data. I used accuracy scores, a confusion matrix, and a classification report to see how well the model worked. 

## Results

* Machine Learning Model:
  * Accuracy -- 95%
  * Precision -- 100% for healthy loans, 85% for high risk loans
  * Recall -- 99% for healthy loans, 91% for high risk loans
  * F1 -- 100% for healthy loans, 88% for high risk loans 

## Summary

The model works very well for predicting which loans are healthy, but not as well for predicting which loans are at high risk for defaulting. Since the purpose of the model is to determine which borrowers to approve for loans, I think the accurate prediction of high risk loans is quite important. The model missed almost 10% of the high risk loans. I woudl not recommend this model. I think it would be better to try and find a more accurate model 