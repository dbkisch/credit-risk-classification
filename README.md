# Module 21 Credit Risk Classification Report

## Overview of the Analysis

* The purpose of this challenge is to demonstrate various techniques to train and evaluate a model based on loan risk.

* The dataset used to build this model, "lending_data.csv", was provided from a peer-to-peer lending services company. The model uses this historical lending data to identify the creditworthiness of borrowers.

* The following independent variables are fed into the model: loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, number of derogatory marks, total debt; the model then predicts whether the loan status will be 0 (healthy) or 1 (high-risk).

* The stages of the machine learning process that comprise this analysis are as follows:
    1. Split the Data into Training and Testing Sets
        * Step 1: Read the `lending_data.csv` data from the `Resources` folder into a Pandas DataFrame.
        * Step 2: Create the labels set (`y`)  from the “loan_status” column, and then create the features (`X`) DataFrame from the remaining columns.
        * Step 3: Split the data into training and testing datasets by using `train_test_split`.
    2. Create a Logistic Regression Model with the Original Data
        * Step 1: Fit a logistic regression model by using the training data (`X_train` and `y_train`).
        * Step 2: Save the predictions on the testing data labels by using the testing feature data (`X_test`) and the fitted model.
        * Step 3: Evaluate the model’s performance:
            * Generate a confusion matrix.
            * Print the classification report.

* The `LogisticRegression` method was used to create this model.

## Results of the Machine Learning Model

* Training dataset
    * Accuracy: 99%
    * Precision: Healthy - 100%, High-Risk - 86%
    * Recall: Health - 99% , High-Risk - 94%

* Testing dataset
    * Accuracy: 99%
    * Precision: Healthy - 100%, High-Risk - 85%
    * Recall: Healthy - 99%, High-Risk - 94%

## Summary

* Results for the training and testing data were virtually the same, which indicates the model will perform as expected in production. 

* The model is highly accurate: the ratio of correctly predicted observations to the total number of observations is 99%.
* In terms of precision, of all the loans classified as High-Risk, 85-86% are actually High-Risk (meaning 14-15% were falsely identified as High-Risk)
* In terms of recall, 94% of High-Risk loans were correctly classified (meaning 6% were incorrectly classified as Healthy)

* I would recommend use of this model due to it's reliability, but would also recommend a secondary test to validate whether a loan is actually High-Risk before administering any corrective actions.
