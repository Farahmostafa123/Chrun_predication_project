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
4. [Model Interpretability](#model-interpretability)
5. [Model Comparison](#model-comparison)
6. [Results](#results)

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

### Model Evaluation Metrics:
For each model, we evaluated:
- **Accuracy**
- **Precision**
- **Recall**
- **F1 Score**
- **AUC (Area Under Curve)**

Confusion matrix visualizations were also generated to evaluate the performance of each model.

---

## Model Interpretability

### SHAP (SHapley Additive exPlanations)
SHAP was used to explain the global and local predictions made by each model. The feature importance plots show how each feature impacts churn prediction.

### LIME (Local Interpretable Model-agnostic Explanations)
LIME was used for local explanations of individual predictions. For each model, LIME explained how specific feature values influenced the churn prediction.

### Partial Dependence Plots (PDP) and Individual Conditional Expectation (ICE)
PDP and ICE plots were used to show the relationship between specific features and churn predictions across the dataset. These plots provide insights into how changes in individual features affect the model’s prediction.

---

## Model Comparison

We compared all the models based on several evaluation metrics, including:
- **Accuracy**
- **Precision**
- **Recall**
- **F1 Score**
- **ROC AUC**

The comparison results were visualized using radar charts and bar plots, providing an easy-to-understand summary of model performance.

---

## Results

### Best Performing Models:
- **XGBoost**, **CatBoost**, and **LightGBM** consistently performed the best across all metrics, showing their strong ability to capture churn patterns.
- **Neural Network (MLP)** performed closely to the ensemble models but showed slightly lower recall and F1 scores.
- **Logistic Regression** and **Decision Tree** showed weaker performance, especially in recall and ROC AUC, indicating that they may not capture the minority (churn) class as effectively.
- **KNN** underperformed across most metrics, particularly in recall and ROC AUC, suggesting it struggled with class boundaries.

### Visualizations:
The performance of the models was compared visually using:
- **Radar charts** to compare multiple metrics.
- **Bar charts** to visualize model accuracy.

---

## How to Run the Code

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/customer-churn-prediction.git
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the cloab notebook for data analysis and modeling:
   ```bash
  
