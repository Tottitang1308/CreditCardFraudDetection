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
