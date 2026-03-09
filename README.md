# Data-Driven Customer Retention Strategy for Interconnect

## Project Overview

Machine learning model predicting telecom customer churn using CatBoost (ROC-AUC: 0.93).

---

## Business Problem

Customer churn reduces long-term revenue and increases customer acquisition costs. The goal of this project is to build a predictive model that identifies customers at high risk of canceling their services so the company can implement targeted retention strategies.

---

## Services Offered by Interconnect

Interconnect provides two main types of services:

* **Landline phone service**
* **Internet service** (DSL or Fiber)

Customers may also subscribe to additional services such as:

* Device Protection
* Online Security
* Technical Support
* Online Backup
* Streaming TV
* Streaming Movies

These services may influence customer satisfaction and churn behavior.

---

## Dataset

The data for this analysis is stored across four separate datasets:

* `contract.csv` — customer contract information
* `personal.csv` — demographic information
* `internet.csv` — internet service details
* `phone.csv` — phone service details

These datasets are merged into a single analytical dataset to enable a comprehensive analysis of customer behavior.

---

## EDA: Key Insights

* Roughly **27%** of customers **churn**
* Monthly **bills** were **higher** for customers who churned
* Customers with service lasting at least **188 days** were **significantly less likely** to churn
* Customers without tech support or online security were **more likely to churn** than those with these services
* Among customers with internet service, those using **fiber optic service** had a **higher churn rate** compared to DSL or no internet service
* Customers on a **month-to-month contract** were nearly **4 times more likely** to churn than those on a one-year contract
* Compared to two-year contracts, month-to-month customers were nearly **15 times more likely** to churn
* Online backup and device protection services did **not** appear to significantly impact churn rates
* **Electronic check payments were strongly associated with churn**, compared to automatic payments or mailed checks

---

## Model Development

Once exploratory analysis was complete, categorical and numerical features were prepared for modeling. A **CatBoost classification model** was selected due to its ability to efficiently handle categorical variables and its strong performance on structured data.

The dataset was split into training and validation sets, and model performance was evaluated using **ROC-AUC**

---

## Model Performance

The CatBoost model achieved strong predictive performance.

| Model              | ROC-AUC  |
| ------------------ | -------- |
| CatBoostClassifier | **0.93** |

A ROC-AUC score of **0.93** indicates excellent separation between customers who churn and those who remain.

---

## Practical Application

The trained CatBoost model could be integrated into Interconnect's customer management system to support proactive retention strategies.

A potential workflow could include:

1. Customer data is updated regularly within the company's database.
2. The churn prediction model evaluates each customer and assigns a churn probability score.
3. Customers with a high predicted churn probability are flagged.
4. The retention team targets these customers with personalized offers such as discounts, service upgrades, or enhanced technical support.

This type of predictive system allows the company to intervene **before customers cancel their services**, improving retention rates and protecting long-term revenue.
