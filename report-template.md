# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

## Results

Logistic Regression Model fitted with Imbalanced Data:

The Logistic Regression model fitted with the Imbalanced DataSet predicted healthy loans 100% of the time and predicted non-healthy loans 85% of the time.


The model fitted with imbalanced data has a higher possibility of making these mistakes:

a healthy loan (low-risk) is classified as a non-healthy loan (high-risk).
a non-healthy loan (high-risk) is classified as a healthy loan (low-risk).

According to the models recall scores, the model made 1% of mistakes when predicting healthy loans and made 9% of mistakes when predicted non-healthy loans.

The model generated an accuracy score of 95% but could be improved due to the dataset being imbalanced.


                                           Logistic Regression Model fitted with Balanced (oversampled) Data:

The Logistic Regression model fitted with the OverSampled DataSet predicted healthy loans 100% of the time and predicted non-healthy loans 84% of the time.


The model fitted with balanced (oversampled) data has a much lower possibility of making these mistakes:

a healthy loan (low-risk) is classified as a non-healthy loan (high-risk).
a non-healthy loan (high-risk) is classified as a healthy loan (low-risk).

According to the models recall scores, the model made 1% of mistakes when predicting healthy loans and made 1% of mistakes when predicted non-healthy loans.

The model generated an accuracy score of 99% due to the dataset being balanced.

## Summary

A lending company might want a model that requires classifying healthy loans and non-healthy loans correctly most of the time:

healthy loans being identified as a non-healthy loan might be more costly for a lending company since it might cause the loss of customers.

non-healthy loans being identified as a healthy loan might also be more costly for a lending company due to the loss of funds being provided by the lender.

The Logistic Regression model fitted with OverSampled data performed much better than the model fitted with Imbalanced data due to the data being balanced and generating a higher accuracy score and a higher recall, indicating that the model will make extremely fewer mistakes when classifying non-healthy loans.


The lending company would most likely want fewer False Positives due to the high possibility of a lender loosing provided funds when classifying non-healthy loans as healthy. The data below is shown in the confusion matrices which indicates how many healthy/non-healthy loans the model predicted correctly/incorrectly.

Model fitted with Imbalanced Data:

56 (FALSE POSITIVES) --> The actual value is healthy and the predicted value is non-healthy

102 (FALSE NEGATIVES) --> The actual value is non-healthy and the predicted value is healthy


Model fitted with Balanced Data:

4 (FALSE POSITIVES) --> The actual value is healthy and the predicted value is non-healthy

116 (FALSE NEGATIVES) --> The actual value is non-healthy and the predicted value is healthy

According to the confusion matrices, the number of False Postives drastically decreases indicating the model will classify healthy & non-healthy loans correctly. Based off of this analysis, I would recommend using Model 2 (Logistic Regression Model fitted with Balanced (oversampled) data.