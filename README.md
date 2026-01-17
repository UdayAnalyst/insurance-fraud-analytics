# Insurance Claims Fraud Analytics

## Overview
This project builds an end-to-end insurance fraud analytics solution to identify and prioritize high-risk insurance claims using statistical modeling and machine learning techniques.

The goal is to support claims investigation workflows by improving fraud detection while aligning predictions with real-world operational constraints.

## Business Problem
Insurance fraud leads to significant financial loss and increased operational costs. Claims investigation teams have limited capacity and must prioritize which claims to review.

This project addresses this challenge by:
- Predicting fraud risk for insurance claims
- Ranking claims by risk
- Flagging only the highest-risk claims for investigation using a Top-K strategy

## Data
- Public insurance claims dataset (Kaggle)
- Structured data including policy details, customer demographics, incident information, and claim amounts
- Target variable: `fraud_reported` (internal insurer fraud classification)

## Methodology
- Data cleaning and leakage-aware feature selection
- Handling missing values and categorical variables
- Model development and comparison:
  - Logistic Regression
  - Random Forest
  - CatBoost (final model)
- Evaluation using fraud-appropriate metrics:
  - Precision, Recall
  - ROC-AUC
  - PR-AUC
- Business-aligned Top-K threshold tuning

## Results
- Final CatBoost model achieved:
  - **PR-AUC: 0.58**
  - **~65% fraud capture while reviewing only 25% of claims**
- Demonstrated effective trade-off between fraud detection and investigator workload

## Tools & Libraries
- Python
- Pandas, NumPy
- Scikit-learn
- CatBoost
- Matplotlib / Seaborn
- Google Colab

## Key Takeaway
Rather than using a fixed probability threshold, this project applies a Top-K risk-scoring approach to align analytics with real-world insurance operations.

## Future Improvements
- SHAP-based explainability
- Cost-sensitive modeling
- Model monitoring and drift detection
