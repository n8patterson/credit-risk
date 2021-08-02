## Overview of the Analysis

The purpose of this analysis is to correctly identify risky and healthy loans using supervised learning.

Our labeled data included many features such as loan size,	interest rate, borrower income, debt to income, number of accounts, derogatory marks, total debt, and finally our labeled loan status. We built our model around predicting the loan status.

Our original data is very imbalanced with 75,036 healthy loans and 2,500 risky loans. Thus, we use and compare two different models. First we use a regular logistic regression model without resampling. Second, we use a model that uses oversampling.

For both models performed four stages of model, fit, predict, and evaluate.

Finally, we evaluted both models comparing our regular logistic regression vs. our model with resampling using oversampling.

## Results

Below are the results of the balanced accuracy scores, the precision, and recall scores of all the machine learning models used in this analysis.

* Machine Learning Model 1 (Logistic Regression):
  * Accuracy:                   95.20%
  * Precision (minority class): 85%
  * Recall (minority class):    91%

* Machine Learning Model 2 (Logistic Regression with Resampling using Oversampling):
  * Accuracy:                   99.37%
  * Precision (minority class): 84%
  * Recall (minority class):    99%

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

The results regarding accuracy of the minority class are actually mixed when comparing the classifiction reports generated from the predictions with the original data versus the predictions with the resampled data. 

First, the accuracy score higher for the resampled data (99.37% vs 95.20%), meaning that the model using resampled data was better at detecting true positives and true negatives. 

The precision for the minority class is slightly higher with the orignal data (0.85) versus the resampled data (0.84) meaning that the original data was better at detecting loans that were actually risky. 

In terms of the recall, however, the minority class metric using resampled data was much better (0.99 vs 0.91). Meaning that the resampled data correctly clasified a higher percentage of loans that were risky. 

Overall, the model using resampled data was much better at detecting risky loans than the model generated using the original, imbalanced dataset.

So, I would recommend to use the model that uses logistic regression with resampling using oversampling as it is more important to correctly identify risky loans over healthy loans.