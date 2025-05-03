# Customer Churn Prediction
This repository contains the code and methodology for predicting customer churn in a telecom company. The project utilizes various machine learning models, feature engineering techniques, and model evaluation methods to predict customer churn. 

## Project Overview

In this project, we use the **Telco Customer Churn** dataset to predict whether a customer will churn or not. The dataset includes customer information such as their demographics, subscription details, service usage, and churn status.

### Key Objectives:
- **Data Preprocessing:** Handle missing values, encode categorical variables, and balance the dataset.
- **Feature Engineering:** Create meaningful features such as Monthly Cost per Tenure, Service Count, Family Package, and others.
- **Modeling:** Train and evaluate multiple machine learning models for churn prediction.
- **Model Interpretability:** Use techniques like SHAP, LIME, PDP, and ICE to explain model decisions.

## Table of Contents

1. [Data Loading and Preprocessing](#data-loading-and-preprocessing)
2. [Feature Engineering](#feature-engineering)
3. [Modeling and Evaluation](#modeling-and-evaluation)

---

## Data Loading and Preprocessing

The dataset used for this analysis is the **Telco Customer Churn** dataset. The following preprocessing steps were applied:

- **Missing Value Handling:**
  - The `TotalCharges` column had missing values, which were replaced with the median value.
  
- **Data Type Conversion:**
  - The `TotalCharges` column was converted to numeric values.

- **Data Balancing:**
  - The dataset was balanced using **SMOTEENN**, which applies a combination of oversampling and undersampling to create a balanced dataset.

- **Categorical Encoding:**
  - Categorical features were encoded using one-hot encoding, and the target variable was label encoded.

---

## Feature Engineering

### 1. Monthly Cost Per Tenure vs Churn
- **X-axis:** Monthly cost per tenure.
- **Y-axis:** Churn status (Churned or Not Churned).
- **Description:** A boxplot was used to visualize the distribution of monthly cost relative to tenure and its correlation with churn.

### 2. Service Count and Churn
- **X-axis:** Number of services subscribed by the customer.
- **Y-axis:** Churn rate.
- **Description:** A bar chart shows churn rates based on the number of services customers subscribe to.

### 3. Family Package (Partner + Dependents) and Churn
- **X-axis:** Whether the customer subscribes to a family package (binary: Yes/No).
- **Y-axis:** Churn rate.
- **Description:** Countplot analysis for churn rate based on family package subscription.

### 4. Short-Term Contract and Paperless Billing
- **X-axis:** Short-term contract and paperless billing (binary: Yes/No).
- **Y-axis:** Churn rate.
- **Description:** A bar plot visualizes churn distribution based on contract and billing type.

### 5. Discount Score (Average Monthly Charges - Actual Charges)
- **X-axis:** Discount score (difference between average and actual monthly charges).
- **Y-axis:** Churn status (Churned or Not Churned).
- **Description:** Violin plot analysis of the discount score distribution based on churn status.

---

## Modeling and Evaluation

### Models Trained:
- **Logistic Regression**
- **Random Forest**
- **Decision Tree**
- **CatBoost**
- **XGBoost**
- **LightGBM**
- **KNN**
- **Neural Network (MLP)**
- **GMM-ASVM**
- **BiLSTM Classifier**
- **SGB**
- **EGBM**

### Model Evaluation Metrics:
For each model, we evaluated:
- **Accuracy**
- **Precision**
- **Recall**
- **F1 Score**
- **AUC (Area Under Curve)**

Confusion matrix visualizations were also generated to evaluate the performance of each model.

---


## How to Run the Code

1. Clone the repository
2. Download files
3. Run on Google Colab
