# 💳 Credit Card Fraud Detection with Cybersecurity Enhancements

## 👨‍💻 Team Members
- Idhant  
- Akshon  
- Harshmit  

---

## 📌 Overview
Credit card fraud is a major concern in the financial industry. This project uses **machine learning** to detect fraudulent transactions and ties the results into the **cybersecurity context**, aiming to flag malicious behavior in real time.

---

## 🎯 Objective
- Build a machine learning pipeline to classify transactions as **fraudulent** or **legitimate**.
- Handle **imbalanced data** effectively.
- Evaluate different classification algorithms.
- Integrate insights with **cybersecurity best practices**.

---

## 🗃️ Dataset

- **Source**: [Credit Card Fraud Detection Dataset on Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- **Size**: 284,807 transactions  
- **Features**: 31  
  - `Time`, `Amount`, anonymized features `V1–V28`, and `Class`
- **Class Label**:
  - `0` = Legitimate  
  - `1` = Fraudulent (~0.17%)

---

## 🧪 Methodology

### 🔹 Preprocessing
- Standardized `Time` and `Amount` using `StandardScaler`.
- Addressed class imbalance using **SMOTE (Synthetic Minority Oversampling Technique)**.

### 🔹 Models Used
| Model                  | Notes |
|------------------------|-------|
| Logistic Regression    | Fast and interpretable baseline model |
| Random Forest          | Handles imbalance, nonlinear patterns |
| XGBoost                | High performance gradient boosting |
| Support Vector Machine | Effective in high-dimensional space |
| K-Nearest Neighbors    | Simple but computationally expensive |

---

## 📊 Evaluation Metrics
- **Accuracy** *(not reliable alone due to imbalance)*
- ✅ **Precision**
- ✅ **Recall**
- ✅ **F1 Score**
- ✅ **Confusion Matrix**

> 🔍 F1 Score is the main metric used, as it balances false positives and false negatives.

---

## 🔐 Cybersecurity Context
Fraud detection models support:
- Real-time transaction monitoring
- Integration with **SIEM tools**
- Behavior-based risk detection (IP changes, device fingerprinting)

---

## 📈 Results & Insights
- **Random Forest** and **XGBoost** outperformed logistic regression.
- Ensemble methods provide better generalization and robustness.
- F1 Scores for best models were above 0.85 after SMOTE.

---

## 🔮 Future Work
- 📦 Model Stacking (combine multiple models)
- 🌍 Integrate geolocation, IP address, and device metadata
- 🔐 Embed detection pipeline into cybersecurity tools for real-time alerts

---

## 🚀 How to Run

1. Clone this repo  
2. Make sure to install required libraries:
   ```bash
   pip install pandas scikit-learn xgboost imbalanced-learn matplotlib
