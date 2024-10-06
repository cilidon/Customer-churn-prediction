# Customer Churn Prediction Project

## Reason Behind the Project
The primary goal of this project was to develop a predictive model to identify customers at risk of churning. By accurately predicting churn, the company can proactively implement retention strategies, reduce customer attrition, and ultimately increase revenue and customer lifetime value.

## Background and Overview
Customer churn is a critical issue in the telecommunications industry, where acquiring new customers is often more expensive than retaining existing ones. This project aimed to leverage machine learning techniques to analyze customer data and predict which customers are likely to discontinue their services.

## Data Structure Overview
The dataset used in this project contained various customer attributes, including:
- **Demographic information** (e.g., gender, senior citizen status)
- **Account information** (e.g., tenure, contract type, payment method)
- **Service usage** (e.g., internet service type, phone service, additional features)
- **Billing information** (e.g., monthly charges, total charges)
- **Churn status** (target variable)

## Executive Summary
We developed and compared four machine learning models to predict customer churn:
1. Logistic Regression
2. Random Forest
3. XGBoost
4. LightGBM

The Logistic Regression model outperformed the others, achieving:
- **Accuracy:** 82.26%
- **Precision:** 69.28%
- **Recall:** 59.25%
- **F1 Score:** 63.87%
- **ROC AUC:** 0.8653

This model provides a strong foundation for identifying customers at risk of churning, allowing for targeted retention efforts.

## Insights Deep Dive
1. **Customer Tenure:** Longer-tenured customers are less likely to churn.
2. **Contract Type:** Customers on month-to-month contracts are more likely to churn.
3. **Additional Services:** Customers with more services are less likely to churn.
4. **Payment Method:** Electronic check users show a higher propensity to churn.
5. **Internet Service:** The type of internet service significantly influences churn risk.

## Key Findings
1. The most important predictors of churn are tenure, contract type, and total charges.
2. There's a strong relationship between customer engagement (number of services) and churn risk.
3. Billing practices and payment methods play a significant role in customer retention.
4. The model can identify high-risk customers with 69.28% precision and 59.25% recall.

## Recommendations
1. Promote longer-term contracts, especially to customers currently on month-to-month plans.
2. Develop targeted retention campaigns for customers in their first year of service.
3. Encourage adoption of additional services through bundling and promotional offers.
4. Investigate issues related to electronic check payments to reduce associated churn.
5. Implement proactive customer service outreach to high-risk customers identified by the model.
6. Consider offering loyalty rewards or discounts to long-term customers.

## Assumptions and Caveats
1. The model assumes that historical patterns of churn will continue in the future.
2. The accuracy of predictions depends on the quality and comprehensiveness of the input data.
3. External factors not captured in the dataset may influence churn.
4. The model should be regularly retrained with new data to maintain its predictive power.
5. While the model is a powerful tool for identifying at-risk customers, human judgment should still play a role in retention strategies.

By implementing these recommendations and leveraging the insights from the churn prediction model, the company can significantly improve customer retention, enhance customer satisfaction, and drive long-term business growth.
