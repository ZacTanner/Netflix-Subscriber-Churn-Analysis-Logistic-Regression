# Netflix Subscriber Churn Analysis (Logistic Regression)

## Overview

This project builds an interpretable logistic regression model to predict subscriber churn and identify key drivers, enabling targeted retention strategies. The data set used for this analysis was obtained from [Kaggle](https://www.kaggle.com/datasets/abdulwadood11220/netflix-customer-churn-dataset/data).

## Model Performance
- ROC AUC: 0.822 (strong predictive power)
- Optimised for recall (F2 score) to prioritise catching churners over minimizing false positives
- Chosen for interpretability via odds ratios

## Key Drivers of Churn
- Inactivity (strongest signal):
- 31–60 days inactive → ~5× higher churn risk
- 8–30 days inactive → +63% higher risk
- Payment method:
- Gift card / crypto users → ~33–34% higher churn
- Account structure:
- Each additional profile → ~37% lower churn
- Subscription tier:
- Premium users churn less than basic users
- Data Considerations
- Excluded avg_watch_time_per_day and watch_hours due to data leakage risk (capturing post-churn behavior)
- High-Risk Segment

**Customers most likely to churn:** Inactive (31–60 days) + non-recurring payment + single profile + basic tier

## Recommended Actions
- Target inactive users with re-engagement campaigns
- Intervene early (8–30 day inactivity window)
- Convert non-recurring payments to subscriptions
- Encourage multi-profile usage
- Promote premium tier upgrades
