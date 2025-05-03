# 💳 Credit Card Fraud Detection 🕵️‍♂️

This project focuses on building machine learning models to detect fraudulent credit card transactions.  
Since fraud cases are extremely rare (~0.2%), special techniques are applied to handle **class imbalance** and improve detection.

---

## 📚 Dataset Info
- Source: Credit Card Transactions dataset
- Total Rows: 284,807
- Features: V1 to V28 (PCA components), `Amount`
- Target: `Class` (0 = Genuine, 1 = Fraud)

> ⚠️ Fraud cases are only ~0.17% of the total data → making this a highly imbalanced classification task.

---

## 🛠️ Steps Followed
1. **Data Loading and Exploration**
2. **Feature Scaling**
   - Normalized the `Amount` column using `StandardScaler`
3. **Train-Test Split**
   - Used `stratify=y` to maintain class proportion
4. **Handled Class Imbalance**
   - Applied **SMOTE (Synthetic Minority Oversampling Technique)** to oversample fraud cases
5. **Trained Multiple Models**
   - Logistic Regression
   - Random Forest Classifier
   - XGBoost Classifier
6. **Evaluated Models using Precision, Recall, F1-Score**
   - Focused on metrics for the Fraud Class (`Class=1`)

---

## 📊 Model Performance Metrics

| Model                | Precision (Fraud Class) | Recall (Fraud Class) | F1-Score (Fraud Class) |
|----------------------|-------------------------|----------------------|------------------------|
| **Logistic Regression**  | 0.40                    | 0.86                 | 0.55                   |
| **Random Forest**        | 0.40                    | 0.86                 | 0.55                   |
| **XGBoost**              | 0.99                    | 0.8                 | 0.77                   |

> ✅ **XGBoost**  performed best, achieving **80% recall** and **77% F1-score** on fraud detection.  
>**Random Forest** also performed strongly, slightly below Random Forest but better than Logistic Regression.

---

## 📝 Key Notes
- All models showed high overall accuracy, but we focused on **Recall and F1-Score** for fraud class (`Class=1`).
- **SMOTE oversampling** was critical in balancing the dataset and preventing models from biasing towards genuine transactions.
- Random Forest outperformed both Logistic Regression and XGBoost, especially in **recall** (catching more fraud cases).
- XGBoost is competitive and is often used in production systems.

---

## 🚀 Conclusion
- **XGBoost** classifier is recommended for production due to its strong fraud detection ability.
- **Random Forest** is a good alternative, slightly trading recall for precision.
- Oversampling (SMOTE) and focusing on recall/F1-score are essential for solving imbalanced problems like fraud detection.

---
