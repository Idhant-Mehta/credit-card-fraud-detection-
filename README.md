# 💳 Credit Card Fraud Detection Using Machine Learning

Detecting fraudulent credit card transactions using machine learning techniques on a real-world imbalanced dataset.

---

## 📌 Overview

This project uses multiple machine learning models to classify credit card transactions as legitimate or fraudulent. The dataset is highly imbalanced, so special techniques like **SMOTE** are used to improve detection of rare fraudulent events.

---

## 🗃️ Dataset

- **Source**: [Kaggle – Credit Card Fraud Detection Dataset 2023](https://www.kaggle.com/datasets/nelgiriyewithana/credit-card-fraud-detection-dataset-2023)
- **Records**: 284,807 transactions  
- **Features**: 31 (`Time`, `Amount`, `V1–V28`, `Class`)
- **Target**: `Class` (0 = Legitimate, 1 = Fraudulent)

📝 **Note**: Download the dataset manually and place `creditcard.csv` inside the `/data` folder.

---

## 🧪 Methodology

### 🔹 Preprocessing
- Standardized `Time` and `Amount` using `StandardScaler`.
- Addressed imbalance using **SMOTE**.

### 🔹 Models Trained
- Logistic Regression
- Random Forest
- XGBoost
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)

### 🔹 Metrics Used
- Precision
- Recall
- F1 Score
- Confusion Matrix

> Accuracy is avoided due to data imbalance. **F1 Score** is prioritized.

---

## 📈 Results

- Best performance by **Random Forest** and **XGBoost** with F1 scores > 0.85.
- SMOTE significantly boosted detection accuracy on minority class.

---

## 🚀 Getting Started

### Step 1: Clone Repository
```bash
git clone https://github.com/yourusername/credit-card-fraud-detection.git
cd credit-card-fraud-detection
pip install -r requirements.txt
python fraud_detection_pipeline.py

