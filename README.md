# Credit Risk Analysis Report 

## Overview of the Analysis

This analysis has the purpose of assessing a set of data about potential borrowers to determine their creditworthiness and the risk assocaited with a potential loan.

The data set contains historical lending activity from a lending services company.
The data includes a range of financal information including: 
 - loan size,
 - interest rate,
 - borrower income,
 - a debt to income ratio, 
 - the number of accounts a borrower holds, 
 - any recorded derogatory remarks, 
 - total debt. 

 These all provide an insight into a borrowers likely ability to pay back a loan.

The model aims to predict, based on all these factors, whether a loan is likley to be healthy (0), or high-risk (1).

The model was given the y variable of the loan status column and the rest of the dataframe was fed into the x variable. And the data was split into training and testing datasets. This was then fitted to a logistic regression model.


## Results

The results from the model were fairly encouraging about the models useability.

On testing the model showed
 - True Postive: 18663
 - True Negative: 563
 - False Postive: 56
 - False Negative: 102

 These correspond to:
 - 1.00 precision score and 0.99 recall for a (0) healthy loan
 - 0.85 precision score and 0.90 recall for a (1) high risk loan

 The model also has accuracy score 0.99.

## Summary

The model is worth recommending, primarily because it correctly identifies if a loan is healthy or risky 99% of the time.

The model is very good at knowing when a loan will be healthy, and that makes sense from the raw data becuase there is significantly more data for those loans. And the majority of loans histroically have been healthy and paid off.

The model is less good when it comes to correctly identifying high risk loans, but it is still correct almost 90% of the time. The model is almost twice as likely to suggest a loan is risky when it is not, than the other way round. This does not beenfit the borrower as it might mean they are marked as a risky investment when they are not. However this does beefit the lending companies when only a minority of supposedly healthy loans turn out to be high-risk.

It might be that to fully recommend this model it is best for lending companies to have a secondary check of some sort on high-risk loans before moving forwards. But to predict healthy loans with almost 100% certainty is very reliable.

The model could be improved by collected more data about high-risk loans, because there is compartively little data about them that is what makes them harder to predict.
