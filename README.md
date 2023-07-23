# Loan Approval Predictions
This notebook is just playing around with a dataset provided at Kaggle.

## About the Data
The data provides information such as income, loan amount, worth in assets, number of dependents, self-employed status, etc, along with labels for loan status.
This data was used to make accurate predictions for which applicants would be accepted for loan repayments.

## Data Cleaning and Preparation
The data was cleaned by performing the following:
- Scaling the continuous data
- Added an extra column for income category
- Encoded discrete values to One Hot Vectors
- Removed the **loan_id** column

## Models Used
The following models were used on the dataset:
- Decision Tree
- Random Forest
- Logistic Regression
- Shallow Neural Network (approximately 30 nodes)

## Findings
- The mutual information for just the **cibil_score** column was very high, and thus had very high correlation with the loan approvals
- When the **cibil_score** column was removed, the models performed poorly for predictions, either showing huge overfitting or underfitting
- Decision Tree performed the best, because obviously it could almost create a decision stump on just the **cibil_score** alone and predict very accurately
