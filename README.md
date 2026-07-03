# Customer Churn Prediction

Machine learning project predicting which telecom customers are likely 
to cancel their subscription, using the IBM Telco Customer Churn dataset 
of 7,032 customers.

## Project Overview
Customer churn is one of the most costly problems in subscription businesses. 
This project builds and compares three classification models to identify 
at-risk customers before they leave, giving the business time to intervene 
with targeted retention offers.

## Key Findings

| # | Theme | Finding |
|---|-------|---------|
| 1 | Churn Rate | 26.6% of customers churned — roughly 1 in 4 |
| 2 | Contract Type | Month-to-month customers churn at 42% vs 3% for two-year contracts |
| 3 | Tenure | Most churners leave within the first 10 months |
| 4 | Monthly Charges | Higher-paying customers churn more — price sensitivity is a key driver |
| 5 | Best Model | Logistic Regression achieved the best ROC-AUC (0.832) |
| 6 | Best Recall | XGBoost caught the most actual churners (recall = 0.626) |

## Models Used

Three classification models were trained and compared:

- **Logistic Regression** — used as a simple, interpretable baseline. 
  Achieved the best overall ROC-AUC of 0.832, showing that on clean 
  structured data, simpler models can outperform complex ones.

- **Random Forest** — an ensemble of 100 decision trees built in parallel. 
  Achieved ROC-AUC of 0.815 and churn recall of 0.473.

- **XGBoost** — added as a third model to widen the comparison and because 
  it is one of the most widely used algorithms in industry for structured 
  tabular data. Unlike Random Forest which builds trees independently, 
  XGBoost builds trees sequentially — each one learning from the mistakes 
  of the previous. It achieved the highest churn recall of 0.626, meaning 
  it caught the most actual churners, making it the preferred model if the 
  business priority is minimising missed churn cases.

## Model Comparison

| Model | Accuracy | ROC-AUC | Churn Recall |
|-------|----------|---------|--------------|
| Logistic Regression | 78.9% | 0.832 | 0.516 |
| Random Forest | 78.5% | 0.815 | 0.473 |
| XGBoost | 73.1% | 0.800 | 0.626 |

## Tools Used
Python, pandas, numpy, matplotlib, seaborn, scikit-learn, XGBoost

## Dataset
[IBM Telco Customer Churn — Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
