# 🛒 Online Shoppers Purchase Prediction (ML Project)

This project predicts whether a user will make a purchase on an e-commerce website based on their browsing behavior using Machine Learning techniques.

---

## 📌 Project Overview

The goal of this project is to analyze user session data and build a classification model to predict **Revenue (purchase or not)**.

We perform:
- Data preprocessing
- Feature engineering
- Handling class imbalance
- Model comparison
- Final model evaluation

---

## 📂 Dataset

- Source: Online Shoppers Intention Dataset
- Records: 12,330 user sessions
- Target Variable: `Revenue`
  - 1 → Purchase made
  - 0 → No purchase

---

## ⚙️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Imbalanced-learn (SMOTE)

---

## 🧹 Data Preprocessing

- Converted categorical variables to numerical format
- Encoded `Month` using Ordinal Encoding
- Converted boolean columns to binary (0/1)
- Removed unnecessary columns
- Feature correlation analysis

---

## ⚖️ Handling Class Imbalance

Used **SMOTE (Synthetic Minority Oversampling Technique)** to balance dataset before training models.

---

## 🔧 Machine Learning Pipeline

The pipeline includes:

1. Missing Value Imputation
2. Feature Scaling (MinMaxScaler)
3. One-Hot Encoding
4. SMOTE Oversampling
5. Feature Selection (SelectKBest - Chi2)
6. Model Training

---

## 🤖 Models Tested

- Random Forest Classifier
- Decision Tree Classifier
- K-Nearest Neighbors
- Ridge Classifier
- Bernoulli Naive Bayes
- Support Vector Machine (SVC)

---

## 🏆 Best Model

| Model | ROC-AUC Score |
|------|--------------|
| SVC | **0.889** |

SVC performed best and was selected as the final model.

---

## 📊 Final Evaluation

- Accuracy: **87%**
- ROC-AUC: **0.78**
- F1 Score: **0.64**

---

## 📈 Key Insights

- `PageValues` is the most important feature for predicting purchases.
- Users with higher exit/bounce rates are less likely to purchase.
- Data is highly imbalanced (majority = no purchase).

---

## 🚀 How to Run

```bash
pip install -r requirements.txt
python main.py
