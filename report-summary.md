
## Overview of the Analysis

The purpose of this analysis was to develop machine learning models to predict loan status based on financial information. The data provided contained information related to loans, and the goal was to predict whether a loan is classified as a healthy loan (label 0) or a high-risk loan (label 1).

Here is some basic information about the variables we were trying to predict:

Label 0 (healthy loan) value count: 18,765 instances
Label 1 (high-risk loan) value count: 619 instances

Features: loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks, and total debt

The analysis went through the following stages of the machine learning process:

- First we had to prepare the data to be able to build a model for it. The lending data was loaded into a DataFrame and divided into features (X) and labels (y). The original data had an imbalanced class distribution, with a significantly higher number of healthy loans compared to high-risk loans.
- We then resampled the dataframe to address the class imbalance using the RandomOverSampler technique.  the minority class (high-risk loans) was overbalanced to improve the class distribution.
- Next we trained the model using Logistic Regression for the resampled training data. 
- Lastly we evaluated the model using various metrics like precision, recall, and F1-score, to assess their performance in predicting both healthy loans and high-risk loans.


## Results

First Regression: 

Accuracy Score: 0.99
Precision for label 0 (healthy loan): 1.00
Precision for label 1 (high-risk loan): 0.85
Recall for label 0 (healthy loan): 0.99
Recall for label 1 (high-risk loan): 0.91


Logistic Regression with Oversampled Data: 

Accuracy Score: 0.99
Precision for 0 (healthy loan): 1.00
Precision for 1 (high-risk loan): 0.84
Recall for 0 (healthy loan): 0.99
Recall for 1 (high-risk loan): 0.99


## Summary



Both models have high accuracy scores, indicating strong overall performance in predicting loan status. They also exhibit high precision for identifying healthy loans, with Model 1 achieving a precision of 1.00 and Model 2 with oversampling achieving a precision of 1.00 as well. For identifying high-risk loans, Model 1 achieves a precision of 0.84, while Model 2 achieves a slightly higher precision of 0.85.

Either Model 1 or Model 2 could be considered as both demonstrate strong performance. It is better to incorrectly predict a healthy loan as high-risk than to predict a high-risk loan as healthy and both models do exceptionally well at that. However, the model with Oversamplig is slightly more accurate for not falsely labling healthy loans as high-risk.