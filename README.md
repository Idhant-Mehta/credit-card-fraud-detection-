# 💳 Credit Card Fraud Detection Using Machine Learning

Detecting fraudulent credit card transactions using machine learning techniques on a real-world, highly imbalanced dataset.

---

## 📌 Overview

This project builds and evaluates multiple machine learning models to classify credit card transactions as legitimate or fraudulent. Because the dataset is extremely imbalanced, the workflow emphasizes techniques like resampling (SMOTE) and metrics that are more informative than accuracy.

Models explored include Logistic Regression, Random Forest, XGBoost, SVM, and KNN. All the work is organized in a single Jupyter notebook for ease of exploration and reproducibility.

---

## 🗃️ Dataset

- Source: Kaggle – Credit Card Fraud Detection Dataset 2023: https://www.kaggle.com/datasets/nelgiriyewithana/credit-card-fraud-detection-dataset-2023
- Records: ~284,807 transactions
- Features: 31 (`Time`, `Amount`, `V1–V28`, `Class`)
- Target: `Class` (0 = Legitimate, 1 = Fraudulent)

Note: Download the dataset manually and place `creditcard.csv` inside a local `data/` folder (not committed to the repo).

---

## 🧪 Methodology

### Preprocessing
- Standardize `Time` and `Amount` using `StandardScaler`.
- Address class imbalance with SMOTE on the training set.

### Models
- Logistic Regression
- Random Forest
- XGBoost
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)

### Evaluation Metrics
- Precision
- Recall
- F1 Score
- Confusion Matrix

Why not accuracy? With a severe class imbalance, accuracy can be misleading. F1 (and Recall for fraud class) are prioritized.

---

## 📈 Results (Summary)

Tree-based models (Random Forest, XGBoost) typically perform best for this dataset, offering strong recall/F1 on the minority (fraud) class when combined with SMOTE. See the notebook for exact numbers and confusion matrices produced during evaluation.

---

## 🚀 Getting Started

### 1) Clone the repository
```bash
git clone https://github.com/Idhant-Mehta/credit-card-fraud-detection-.git
cd credit-card-fraud-detection-
```

### 2) Create a virtual environment (recommended)
```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate
```

### 3) Install dependencies
If you don’t have a `requirements.txt`, install the core packages:
```bash
pip install jupyter pandas numpy scikit-learn imbalanced-learn xgboost matplotlib seaborn
```

### 4) Add the dataset
Place `creditcard.csv` at:
```
./data/creditcard.csv
```

### 5) Run the notebook
Open Jupyter and run the cells in order:
```bash
jupyter notebook
```
Then open:
```
Project_10_Credit_Card_Fraud_Detection_Cybersecurity_Enhanced.ipynb
```

---

## 📁 Repository Structure

```
credit-card-fraud-detection-/
├─ Project_10_Credit_Card_Fraud_Detection_Cybersecurity_Enhanced.ipynb   # Main notebook with full pipeline
├─ README.md                                                              # This file
└─ data/                                                                  # (local only) place creditcard.csv here
```

---

## 🔍 Notes on Imbalance & Thresholds
- Use SMOTE only on the training split to avoid data leakage.
- Consider threshold tuning to increase recall (at the cost of precision) depending on business requirements.
- Precision–Recall curves are often more informative than ROC curves for this problem.

---

## 🙌 Acknowledgements
- Dataset: Kaggle community; originally derived from the well-known anonymized credit card dataset.

---


