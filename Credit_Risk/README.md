# Credit Risk Analysis Report

The code implementation for this analysis is contained in the [`credit_risk_classification.ipynb`](credit_risk_classification.ipynb) file.

## Overview of the Analysis

This analysis aims to assess the **creditworthiness of borrowers** based on historical lending data from a peer-to-peer lending platform. Using machine learning, we build a **logistic regression model** to predict the likelihood of loan default, which helps lending institutions make informed decisions.

The dataset contains financial details about loans, with a `loan_status` column serving as the target variable:
- `0`: Healthy loan
- `1`: High-risk loan

### Steps in the Analysis:
1. **Data Preparation** – Loaded the dataset, defined features (`X`) and labels (`y`)
2. **Splitting Data** - Split the features and labels into training/testing datasets.
3. **Model Training** – Applied **Logistic Regression** to the training data.
4. **Evaluation** – Assessed the model using a **classification report** and **confusion matrix**.

## Results

### Model Performance Metrics:
- **Accuracy Score:** 99%  
- **Precision (Healthy Loans - `0`)**: 100%  
- **Precision (High-Risk Loans - `1`)**: 84%  
- **Recall (Healthy Loans - `0`)**: 99%  
- **Recall (High-Risk Loans - `1`)**: 94%  
- **Macro Average F1-Score:** 94%  
- **Weighted Average F1-Score:** 99%  

### Confusion Matrix Insights:
| Actual \ Predicted | Predicted 0 | Predicted 1 |
|--------------------|------------|------------|
| **Actual 0**      | 18,658     | 107        |
| **Actual 1**      | 37         | 582        |

## Summary

The **logistic regression model performs exceptionally well**, achieving **99% accuracy**. It correctly classifies **healthy loans (`0`) with near-perfect precision and recall**, meaning most well-performing loans are identified accurately. 

For **high-risk loans (`1`)**, the model maintains strong **recall (94%)**, successfully identifying most borrowers at risk of default. However, its **precision (84%)** indicates that some **healthy loans are incorrectly classified as high-risk**.

### Recommendation:
- If accurately identifying **high-risk borrowers** is the primary concern, this model is **highly effective** due to its **high recall (94%)**.
- If minimizing **false positives** (healthy loans mistakenly labeled as high-risk) is critical, the model still performs **exceptionally well**, with a **low misclassification rate (only 107 cases out of 19,384 loans)**.

This model is **recommended** for credit risk classification due to its high predictive accuracy.