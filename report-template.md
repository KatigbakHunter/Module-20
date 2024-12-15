# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.

The goal of the analysis is to accurately predict the status of a customers loan status. The original dataset cointained a column for loan status for each account that is accounted for as a binary variable. Using a logistic regressor model, we can create a model that can accurately calssify healthy loans vs high-risk loans since logistic regressor are great at classifications.

* Explain what financial information the data was on, and what you needed to predict.

The dataset contained the financial status of a customers. The data that are listed are a customers income, loan size, interest rate for loans, debt to income ratio, number of accounts, deregotory marks made from the customers  credit hsitory, and total debt. 

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
Our target variable is loan status. Using value_counts() we can see the ratio of 75036 to 2500 of healthy vs high-risk loans 
loan_status
0    75036
1     2500
Name: count, dtype: int64

Using balanced_accuracy_score(), when can output a percentage of of healthy loans vs high-risk loans which is 96%
0.9672620331306306

* Describe the stages of the machine learning process you went through as part of this analysis.

After importing a studying the dataset, I seperated the tagret variables and features and assigned X and y variable. For the goal of the model,  using loan_status as the target variable, I used the rest of the features as our x. I then split the data into training to testing data toa train the model. I then created a logistic regression model to fit into the training data while adding a mx_iter of 500 to adress processing issues. After reviewing y_predictions, I then printed a classification report and reviewed the balance of healthy and high-risk loans. 

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).

Using logistic regression as the model was the best fit. WIht our goal of predicting loan status, it was ideal due to a logistic regression model since it is great at classification. Some of the methos I used was train_test_split, to split the training and tes sets. classification reports to review the accuracy of hte model. 


## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1: Logistic Regression 
* Description of Model 1 Accuracy, Precision, and Recall scores.
              precision    recall  f1-score   support

           0      1.00      0.99      1.00     18765
           1       0.84      0.94      0.89       619

    accuracy                           0.99     19384
   macro avg       0.92      0.97      0.94     19384
weighted avg       0.99      0.99      0.99     19384

The precision score tells us that it had a 100% accurate prediction for healthy loand while it is 84% for high-risk loans. The accuracy is the overall precentage of correct predictions. since the recall is 99% this mens that 

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

I do not think I would use any other model unless givena different goal. The logistic regression is great at classification and since loan_status was set as a binary variable, we can use it as our target variable. Rather I would improve the model using standardization. I would also test different weigths of features since features like number of accounts arent as important as data such as bebt to income ratio