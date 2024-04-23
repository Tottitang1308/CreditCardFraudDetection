# FraudAnalytics
Self-learning Fraud Analytics Project

# Credit Card Fraud Detection

## Project Overview
This project aims to identify fraudulent transactions using credit card data. It leverages machine learning techniques to predict whether a given transaction is fraudulent or not. The project is crucial for enhancing security measures and minimizing financial losses due to fraud.

## Motivation
The motivation behind this project is to improve the accuracy of fraud detection in credit card transactions, reduce false positives, and help financial institutions enhance their fraud prevention systems.

## Technologies Used
- Python 3.8
- Pandas
- NumPy
- Scikit-learn
- Matplotlib (for visualization)
- Jupyter Notebook

## Dataset
The dataset used in this project consists of transactions made by credit cards in September 2013 by European cardholders. It presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, with the positive class (frauds) accounting for 0.172% of all transactions.

## Features
The dataset contains only numerical input variables which are the result of a PCA transformation. Unfortunately, due to confidentiality issues, the original features and more background information about the data are not provided.

- `V1, V2, ... V28`: PCA transformed features.
- `Time`: Number of seconds elapsed between this transaction and the first transaction in the dataset.
- `Amount`: Transaction amount.
- `Class`: 1 in case of fraud and 0 otherwise.

## Model
The model used is a Random Forest Classifier. A GridSearchCV was employed to tune the hyperparameters and improve the model's recall to effectively predict more fraud cases.

## Results:

### Fraud Detection Model Performance Report
#### Overview:
Our latest fraud detection system has been evaluated to determine its accuracy in identifying fraudulent credit card transactions.

#### Results:

- The system correctly identified 56,855 normal transactions with a very high degree of accuracy (True Negative).
- It successfully flagged 78 transactions as fraudulent, which were confirmed to be true cases of fraud (True Positive).
- Notably, the system erroneously flagged 9 legitimate transactions as fraudulent (False Positive). While this number is low, it indicates that a minimal number of customers might experience inconvenience due to false alarms.
- There were 20 fraudulent transactions that the system did not detect (False Negative). This represents a small window through which fraudulent activity can occur undetected.

#### Impact:

- The low number of false alarms (9 in 56,864) ensures that customer disruption is minimal, preserving trust and satisfaction.
- The detection of 78 out of 98 fraudulent transactions shows that the system is highly effective, potentially preventing significant financial loss.
- The oversight of 20 fraudulent transactions, while relatively small, suggests an area for improvement. Each missed fraud case can carry financial and reputational risks that we must seek to minimize.

This model represents a strong step towards protecting both our customers and our business from the risks of fraudulent transactions.

## Features Importance:

### Interpretation:
- V10: This is the most important feature according to the model. Whatever original variables contribute most heavily to the V10 component are highly predictive of the target variable (likely whether a transaction is fraudulent).
- V14, V12, V17, V11, V4, V16, V7, V3: These follow in descending order of importance. They also play significant roles in the model's decisions, but to a lesser extent than V10.

#### In a Business Context:
- Focus on Transactions: The components like V10, V14, and so on, seem to be the most informative for fraud detection. The business should closely monitor transactions that score highly on these components for potential risk.
- Risk Profiling: Transactions that have higher values in these key components might warrant additional checks or verification steps.
- Resource Allocation: Invest more in tools and techniques that can track or derive features similar to those contributing to the top PCA components.

In summary, this plot can guide a business to prioritize certain aspects of transaction data when considering fraud risk and where to allocate resources for fraud prevention efforts.




##
### End of Report 
##
