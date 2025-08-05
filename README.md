# Telecom Churn Prediction

Predicting customer churn for a telecom provider using contract, internet, and demographic data.

---

## Overview

This project focuses on identifying customers likely to churn using classification models. By predicting churn, telecom providers can proactively improve retention strategies and reduce customer loss.

---

## Data Sources

The project uses four datasets provided by the telecom operator:

- `contract.csv` – Contract type, billing method, monthly/total charges  
- `personal.csv` – Demographics: gender, senior citizen status, partner, dependents  
- `internet.csv` – Internet service usage and add-ons (security, streaming, backup)  
- `phone.csv` – Phone line details  

All datasets were merged on `customerID` using a left join.

---

## Methodology

- Merged and cleaned all datasets (handling missing values, converting types)
- Engineered a binary target variable `is_active` based on `EndDate`
- Performed EDA to identify drivers of churn (e.g., contract type, charges, services)
- One-hot encoded categorical variables and scaled numeric features
- Trained multiple classification models:
  - Logistic Regression
  - LightGBM
  - CatBoost
- Evaluated models using **AUC-ROC** and **Accuracy**

---

## Results

- **Best model:** CatBoost Classifier (with hyperparameter tuning)
- **AUC-ROC:** 0.84+
- Key churn indicators:
  - Customers with **month-to-month contracts**
  - Users with **fiber optic internet**
  - Payment method = **electronic check**
  - Customers lacking **security/tech support add-ons**

---

## Project Files

- `final_project_polished.ipynb` — Full notebook with data prep, EDA, modeling, and results

---

## Key Skills Used

`pandas` • `numpy` • `matplotlib` • `seaborn` • `scikit-learn` • `CatBoost` • `LightGBM` • `XGBoost` • `EDA` • `Feature Engineering` • `AUC-ROC`

---
