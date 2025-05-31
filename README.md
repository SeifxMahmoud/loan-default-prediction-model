# 💳 Loan Default Prediction Using Artificial Neural Networks (ANN)

## 📌 Overview
This project implements an Artificial Neural Network (ANN) for predicting loan repayment outcomes using Lending Club’s historical loan data. It classifies borrowers as either **Fully Paid** or **Charged Off**, based on borrower attributes such as credit score, annual income, employment status, and loan purpose. The final model achieves ~91% accuracy and provides a robust foundation for credit risk scoring applications.

## 🎯 Business Context
Loan default prediction is central to credit risk management, especially in personal lending. Accurate classification helps:
- Lenders reduce exposure to high-risk borrowers,
- Reinsurers model expected credit losses more effectively,
- Investors build robust portfolios of securitized loans (e.g., ABS, CDOs).

This project demonstrates how neural networks can enhance traditional scoring systems through non-linear modeling capabilities.

## 🧠 Problem Statement
Given a dataset of Lending Club borrowers, we aim to:
- Predict whether a loan will be **Fully Paid** or **Charged Off**
- Evaluate the model’s performance using classification metrics
- Interpret the results to inform portfolio risk management strategies

## 🔧 Methodology

### Data Preparation
- **Source**: [Lending Club dataset (Kaggle)](https://www.kaggle.com/datasets/wordsforthewise/lending-club)
- **Features Used**: FICO score, annual income, employment length, term, grade, purpose, loan amount, interest rate, etc.
- **Target Variable**: `loan_status` (converted to binary labels)
- **Preprocessing**:
  - Imputation for missing values
  - One-hot encoding for categorical variables
  - Standardization for numeric features

### Model Architecture
- Input layer with normalized borrower features
- Two hidden layers with ReLU activation
- Output layer with sigmoid activation for binary classification
- Optimizer: Adam  
- Loss Function: Binary Cross-Entropy  
- Evaluation: Accuracy, F1 Score, Confusion Matrix

## 📈 Results

| Metric              | Value   |
|---------------------|---------|
| Accuracy            | ~91%    |
| Precision (Charged Off) | 81%    |
| Recall (Charged Off)    | 78%    |
| F1 Score            | 79.5%   |

## 📊 Confusion Matrix

|                    | Predicted: Fully Paid | Predicted: Charged Off |
|--------------------|------------------------|--------------------------|
| **Actual: Fully Paid**   | 8423                   | 527                      |
| **Actual: Charged Off**  | 634                    | 2194                     |
