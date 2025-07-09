# 🫀 CHD Risk Prediction using Machine Learning

> A machine learning project to predict the **10-year risk of Coronary Heart Disease (CHD)** using clinical data from the Framingham Heart Study.

![Python](https://img.shields.io/badge/Python-3.13-blue?logo=python)
![Status](https://img.shields.io/badge/Status-Completed-green)
![License](https://img.shields.io/badge/License-MIT-blue)

---

## 📌 Overview

This project focuses on developing reliable ML models to predict the 10-year risk of coronary heart disease using real-world patient data. The dataset used is derived from the **Framingham Heart Study**, a landmark cardiovascular research initiative.

---

## 🧠 Project Goals

- Handle missing values and perform proper data cleaning
- Engineer meaningful domain-specific features
- Balance the dataset using **SMOTE**
- Train and evaluate multiple classification models
- Perform **hyperparameter tuning** and **threshold optimization**
- Build a robust **Stacking Ensemble** for better generalization
- Compare models using precision, recall, F1-score, and AUC
- Save models for deployment-ready use

---

## 📂 Dataset

- Source: [Framingham Heart Study Dataset](https://www.kaggle.com/datasets/amanajmera1/framingham-heart-study-dataset)
- Total records: ~3,300 patients
- Target: `TenYearCHD` (0 = No risk, 1 = At risk)

---

## 🔧 Techniques Used

### ✅ Preprocessing & Feature Engineering
- Missing value analysis & imputation
- Outlier handling
- Domain-based features:
  - Blood pressure ratio (`sysBP / diaBP`)
  - Cholesterol-to-age ratio
  - BMI category
  - Smoking level

### ⚖️ Handling Class Imbalance
- Applied **SMOTE** to balance the CHD-positive class (~15% originally)

### 🧪 Models Trained
- Logistic Regression (Base & Tuned)
- Random Forest (Base, Tuned, Threshold-Optimized)
- Stacking Classifier (LogReg + RF → LogReg meta)

---

## 📊 Model Performance Summary (SMOTE Data)

| Model                          | Accuracy | Precision | Recall | F1 Score | AUC  |
|-------------------------------|----------|-----------|--------|----------|------|
| Logistic Regression (Tuned)   | 0.70     | 0.71      | 0.67   | 0.69     | 0.77 |
| Random Forest (Tuned)         | 0.92     | 0.93      | 0.91   | 0.92     | 0.97 |
| Random Forest (Threshold 0.48)| 0.91     | 0.92      | 0.91   | 0.91     | 0.97 |

### ✅ Final Model Selected:
> **Tuned Random Forest with threshold = 0.48**  
> High AUC, balanced F1 score, and robust CHD-positive class detection.

---

