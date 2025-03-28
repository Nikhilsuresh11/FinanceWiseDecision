# FinanceWiseDecision


 This repository contains solutions for bank loan eligibility, credit card fraud detection, and customer segmentation.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Results](#results)
- [License](#license)

## Introduction

This project addresses three key financial challenges:
1. **🏦 Bank Loan Eligibility**: Determine whether an applicant is eligible for a loan.
2. **💳 Credit Card Fraud Detection**: Identify fraudulent transactions to prevent financial loss.
3. **👥 Customer Segmentation**: Segment customers to tailor marketing strategies and improve customer satisfaction.

## Features

- **Machine Learning Models**: Implemented using various algorithms for high accuracy.
- **Data Preprocessing**: Cleaning and transforming raw data for better model performance.
- **Visualization**: Insightful graphs and charts to understand data patterns.
- **Automated Pipelines**: Streamlined workflow for model training and evaluation.

## Installation

To get started, clone the repository and install the necessary dependencies:

```bash
https://github.com/Nikhilsuresh11/FinanceWiseDecision.git
cd finance-wise-decision
pip install -r requirements.txt
```

---


## Results

## Credit Card Fraud Detection Outcomes

### SVM, KNN and Random Forest were not used:
- **SVM**: Inefficient with large datasets due to high computational power and time requirements, especially with K-Fold cross-validation.
- **Random Forest**: Also computationally intensive, hence not used for all hyperparameter tuning with oversampling.
-  **KNN**: KNN is not memory efficient. It becomes very slow as the number of data points increases as the model needs to store all the data points. It is computationally heavy because for a single datapoint the algorithm has to calculate the distance of all the datapoints and find the nearest neighbors.

### Metric Selection for Imbalanced Data:
- **Accuracy**: Not suitable for heavily imbalanced data (only 8.74% fraudulent transactions).
- **ROC-AUC Score**: Preferred for fair evaluation, assessing model performance across all classification thresholds.
- **F1 Score**: Used to measure precision and recall at the optimal threshold.

### Model Selection:
- **Logistic Regression & XGBoost**: Best performers in terms of ROC-AUC score.
- **XGBoost**: Chosen for best performance (ROC 1.0 on train, 0.98 on test) despite higher resource utilization.
- **Logistic Regression**: Less resource-intensive and cost-effective.

### Handling Data Imbalance:
- **Undersampling**: Reduces non-fraudulent transactions to balance class distribution.
- **Oversampling**: Increases fraudulent transactions to balance class distribution.
- **SMOTE**: Uses nearest neighbors to create synthetic data.
- **ADASYN**: Similar to SMOTE, but focuses on low-density regions.

### Cost-Benefit Analysis:
- **Infrastructure and Resources**: High-resource models (Random Forest, SVM, XGBoost) vs. low-resource models (Logistic Regression).
- **Monetary Impact**: Consider cost vs. benefit for small changes in ROC score.

### Business Summary:
- **High Precision**: Preferred for banks with smaller average transaction values to minimize false positives.
- **High Recall**: Essential for banks with larger transaction values to avoid missing high-value fraudulent transactions.
- **Recommendation**: Logistic regression with SMOTE for the balanced dataset, offering good ROC score and high recall. Easier to interpret and explain.

---

## Customer Segmentation Outcomes


## About Dataset

This dataset contains information related to customers and their credit card usage, providing insights into customer behavior, preferences, and usage patterns.

## Objectives

1. Perform data cleaning, preprocessing, visualization, and feature engineering.
2. Implement hierarchical clustering, K-means clustering, and DBSCAN models.

##  Features Description

1. **Sl_No**: Serial number or index for each record.
2. **Customer Key**: Unique identifier for each customer.
3. **Avg_Credit_Limit**: Average credit limit assigned to each customer.
4. **Total_Credit_Cards**: Total number of credit cards held by each customer.
5. **Total_visits_bank**: Total number of visits to a physical bank branch.
6. **Total_visits_online**: Total number of visits to the online banking platform.
7. **Total_calls_made**: Total number of calls made to customer service.

## Results

### Segment Analysis

1. **Segment 0**:
   - Low credit limit, high number of credit cards.
   - Likely high credit usage and low income.
   - Prefers phone calls for complaints.
   - **Target**: Cross-sell via phone calls, and arrange feedback calls from Relationship Managers.

2. **Segment 1**:
   - Few phone calls, highest online visits, no bank visits.
   - Likely literate, premium customers with higher income.
   - **Target**: Luxury offers via emails, online shopping coupons, and potential high-profit customers.

3. **Segment 2**:
   - Median of 3 bank visits, holds 4-6 credit cards.
   - Relatively higher bank visits.
   - **Target**: Cross-sell through in-bank managers, and promotional advertisements in the bank.

### Promotional Strategy

- **Segment 0**: Cross-sell via phone calls.
- **Segment 1**: Luxury offers via emails, and online shopping coupons.
- **Segment 2**: Cross-sell through in-bank managers, and promotional advertisements (Servicescape Promotions).

---
