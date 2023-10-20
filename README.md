# Big-Data-Analytics-Loan-Default-Prediction
Big Data Analytics: Loan Default Prediction with PySpark

Focus
To look into various attributes to try to predict whether a person will be a loan defaulter

Features
- Total: 32
- Categorical: 9 (e.g.Grade, Sub_Grade)
- Continuous: 23 (e.g. Loan_Amount, Funded_Amount)
- Label:  Loan_Status

Data cleansing
- delete non-informative data (e.g. I,,Payment_Plan: has a single entry ‘n’)
- match the mismatch between column names and value types

Modelling (Compared with ROC)
- Baseline: Logistic Regression (0.5053)
  
  Comparing:
 - Simple model:
 1. Random Forest (0.5278)
 2. Naive Bayes (0.5161)
- Ensembled model:
 1. Random Forest + Logistic Regression (0.5472)
 2. Random Forest + Naive Bayes (0.5472)
The ROC of both Ensembled model are the highest among all models, while the ROC of Random Forest is higher than Naive Bayes. Thus would choose Random Forest + Logistic Regression as the most suitable model.

Visualization
- Distribution of the target variable
  Skewness = 0.2743322088940716
  Therefore, the distribution is relatively symmetric
- Feature importance
  Loan_Amount is the most important feature in this random forest model for predicting Loan_Status
- Correlation matrix
- Confusion matrix
  The goal is to have a high number of true positives and true negatives and a low number of false positives and false negatives.


