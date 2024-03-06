## Module 20 Challenge - Credit Risk Analysis Report

Risk Classification

## Table of Contents:

1. Analysis Overview
2. Model Results
3. Summary

## Overview of the Analysis

Lending companies extend credit with the expectation of repayment or return of assets. Credit risk, the likelihood of borrowers defaulting, is a critical factor in financial operations. In this analysis, we leverage machine learning to scrutinize a dataset from a peer-to-peer lending service. The goal is to construct a model that discerns the creditworthiness of borrowers.

Model Selection: 
Utilizing the Logistic Regression Algorithm, a widely employed tool for classification problems, the analysis focuses on categorizing loans as healthy (low-risk) or non-healthy (high-risk) based on loan status.

Initial Model Evaluation: The Logistic Regression Model achieved an impressive 95% accuracy. However, scrutiny revealed a disparity in recall values, with non-healthy loans trailing at 0.91 compared to healthy loans at 0.99. This discrepancy stems from an imbalanced dataset, where healthy loans substantially outweigh non-healthy ones.

Imbalanced Data Insight: A glance at the loan status distribution indicates a highly imbalanced dataset, with healthy loans dominating (75,036) and non-healthy loans trailing (2,500).



# code
y.value_counts()

# output
0    75,036
1    2,500

Confusion Matrix (Imbalanced Data): The model's performance revealed some misclassifications, especially in predicting non-healthy loans.

## Confusion Matrix

## Resampling for Balance: 
To rectify the imbalance, the RandomOverSampler from the imbalanced-learn library is employed to oversample the non-healthy class.


# code
y_oversampled.value_counts()

# output
0    56,271
1    56,271

Improved Model: The Logistic Regression Model fitted with oversampled data delivered a superior accuracy of 99%. Notably, the recall for non-healthy loans surged from 0.91 to 0.99, showcasing improved sensitivity to high-risk cases.

Confusion Matrix (Resampled Data): The revised model displayed enhanced performance, with fewer misclassifications.

## Confusion Matrix

## Results

Logistic Regression Model fitted with Imbalanced Data
 
Model Performance: The imbalanced dataset model predicted healthy loans with 100% accuracy but demonstrated an 85% accuracy for non-healthy loans.

Challenges: This model is prone to mistakes, particularly in misclassifying a healthy loan as non-healthy or vice versa.

Classification Report Imbalanced

Accuracy Score: The overall accuracy stood at 95%, indicating room for improvement due to the dataset's imbalance.

Accuracy Score 95


Logistic Regression Model fitted with Balanced (oversampled)

Model Performance: The oversampled model maintained a 100% accuracy for healthy loans and improved accuracy for non-healthy loans to 84%.

Enhancements: This model showed reduced susceptibility to misclassifications, addressing concerns from the imbalanced dataset.

Classification Report Balanced

Accuracy Score: The balanced dataset model achieved an impressive accuracy of 99%, highlighting the effectiveness of oversampling.

Accuracy Score 99

## Summary

Recommendation: Considering the critical nature of correctly classifying healthy and non-healthy loans, the Logistic Regression Model fitted with Balanced (oversampled) Data is recommended.

Key Considerations:

The balanced model demonstrated heightened accuracy and recall, particularly in identifying non-healthy loans.
False Positive instances decreased significantly, showcasing improved precision in classifying healthy and non-healthy loans.
The lending company's preference for fewer False Positives aligns with the oversampled model's superior performance.
Based on this analysis, the Logistic Regression Model fitted with Balanced (oversampled) Data is the preferred choice for credit risk assessment.





