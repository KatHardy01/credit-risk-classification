# Credit Risk Analysis Report 

## Introduction 
The purpose of this analysis is to build and evaluate machine learning models to predict loan risk: healthy ("low risk") or "high-risk". The goal is to help make informed loan approval decisions based on historical data.

## Overview of the Analysis

The dataset contains financial information about loans, such as loan amount, interest rate, and borrower details. The target variable, `loan_status`, is binary, with `0` representing healthy loans and `1` representing high-risk loans. The dataset shows a significant class imbalance, with more healthy loans than high-risk loans.

The stages of the machine learning process included:
1. Splitting the data into training and testing sets.
2. Standardizing the features to improve model performance.
3. Training and evaluating the Logistic Regression Model.
4. Evaluating the model using metrics such as accuracy, precision, recall, and F1-score.

### Methods:  
**1. Data Preprocessing:**
* Split the dataset into features (`X`) and labels (`y`).
* Use `train_test_split` for training and testing sets.
* Standardize features with `StandardScaler`.

**2. Machine Learning Model:**
* Logistic Regression Model

**3. Model Evaluation:**
* `confusion_matrix`: Used to evaluate the number of true positives, true negatives, false positives, and false negatives for both models.
* `classification_report`: Generated to calculate precision, recall, F1-score, and accuracy for both classes (`0` for healthy loans and `1` for high-risk loans).

## Results
### Machine Learning Model Logistic Regression 
**Confusion Matrix Analysis:**
* Healthy Loans (`0`):
    * True Positives: 18,658
    * False Negatives: 107
    * The model performs exceptionally well in predicting healthy loans, with very few misclassifications.
* High-Risk Loans (`1`):
    * True Positives: 585
    * False Negatives: 34
    * The model is effective at identifying high-risk loans, though it misses a small number of them.

**Classification Report Analysis:**
* Accuracy: 99%
* Precision:
    * `low_risk` (0): 1.00 
    * `high_risk` (1): 0.89 
* Recall:
    * `low_risk` (0): 0.99 
    * `high_risk` (1): 0.95
* F1-Score:
    * `low_risk` (0): 1.00 
    * `high_risk` (1): 0.89
 
## Summary
Overall, I would highly recommend the Logistic Regression for credit risk classification.
