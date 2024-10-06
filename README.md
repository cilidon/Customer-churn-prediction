# Customer Churn Prediction for Telecom company

The primary goal was to develop a predictive model to identify customers at risk of churning. By accurately predicting churn, the company can proactively implement retention strategies, reduce customer attrition, and ultimately increase revenue and customer lifetime value.

## Background and Overview
Customer churn is a critical issue in the telecommunications industry, where acquiring new customers is often more expensive than retaining existing ones. This project aimed to leverage machine learning techniques to analyze customer data and predict which customers are likely to discontinue their services. IBMs telecom dataset was used in this project.

## Data Structure Overview
The dataset used in this project contained various customer attributes, including:
- **Demographic information** (e.g., gender, senior citizen status)
- **Account information** (e.g., tenure, contract type, payment method)
- **Service usage** (e.g., internet service type, phone service, additional features)
- **Billing information** (e.g., monthly charges, total charges)
- **Churn status** (target variable)

The dataset is imbalanced with Churn distribution:

Churn

No     0.73463

Yes    0.26537

To counter imbalance,
1. weights were given to labels to make models learn better.
2. Oversampling( SMOTE ) to add more churned users to make models learn better. 

The models were evaluated after both these techniques.


## Summary
Developed and compared four machine learning models to predict customer churn:
1. Logistic Regression
2. Random Forest
3. XGBoost
4. LightGBM

### Model Comparison

| Model | Technique | Accuracy | Precision | Recall | F1 Score | ROC AUC | Cross-Val ROC AUC |
|-------|-----------|----------|-----------|--------|----------|---------|-------------------|
| Logistic Regression | Class Weighting | 0.7587 | 0.5282 | 0.8284 | 0.6451 | 0.8650 | 0.8426 |
| Logistic Regression | Oversampling | 0.7892 | 0.6484 | 0.4450 | 0.5278 | 0.7927 | 0.9327 |
| Random Forest | Class Weighting | 0.7921 | 0.6460 | 0.4745 | 0.5471 | 0.8369 | 0.8266 |
| XGBoost | Class Weighting | 0.7991 | 0.6415 | 0.5469 | 0.5904 | 0.8375 | 0.8138 |
| LightGBM | Class Weighting | 0.7743 | 0.5516 | 0.7882 | 0.6490 | 0.8554 | 0.8308 |
| LightGBM | Oversampling | 0.8105 | 0.6506 | 0.6139 | 0.6317 | 0.8548 | 0.9377 |

### Best Performing Model
The LightGBM model with oversampling achieved the best overall performance:
- Accuracy: 0.8105
- Precision: 0.6506
- Recall: 0.6139
- F1 Score: 0.6317
- ROC AUC: 0.8548
- Cross-Val ROC AUC: 0.9377

### Feature Importance (LightGBM)
Top 15 Important Features:
1. MonthlyCharges
2. TotalCharges
3. TotalCharges_tenure
4. tenure
5. MonthlyCharges_tenure
6. PaymentMethod_Electronic check
7. gender
8. OnlineBackup_No
9. PaymentMethod_Credit card (automatic)
10. PaymentMethod_Bank transfer (automatic)
11. TechSupport_No
12. OnlineSecurity_No
13. Contract_One year
14. Partner
15. PaperlessBilling

![image](https://github.com/user-attachments/assets/e5efb922-d3fd-4c72-9a47-ff35797b7978)



### Insights Deep Dive
1. Financial factors (charges and tenure) are the most important predictors of churn.
2. Payment method, particularly electronic checks, significantly influences churn risk.
3. The absence of certain services (OnlineBackup, TechSupport, OnlineSecurity) is associated with higher churn risk.
4. Contract type plays a role in customer retention.


### Key Findings
1. The most important predictors of churn are tenure, contract type, and total charges.
2. There's a strong relationship between customer engagement (number of services) and churn risk.
3. Billing practices and payment methods play a significant role in customer retention.
4. The model can identify high-risk customers with 81% Accuracy.

## Recommendations
1. Review and optimize pricing strategies, especially for long-term customers.
2. Implement programs to increase customer tenure and encourage longer contracts.
3. Investigate and address issues related to electronic check payments.
4. Promote service bundles that include OnlineBackup, TechSupport, and OnlineSecurity.
5. Develop targeted retention strategies based on customer segments and risk factors.
6. Implement an early intervention program for high-risk customers.

## Assumptions and Caveats
1. The model assumes that historical patterns of churn will continue in the future.
2. External factors not captured in the dataset may influence churn.

By implementing these recommendations and leveraging the insights from the churn prediction model, the company can significantly improve customer retention, enhance customer satisfaction, and drive long-term business growth.
