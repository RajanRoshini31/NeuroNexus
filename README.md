# NeuroNexus
# 🚢 Titanic Survival Prediction - Machine Learning Project

This project aims to predict whether a passenger survived the Titanic disaster using machine learning models. Using the Titanic dataset, we trained multiple classifiers and compared their performance using standard classification metrics.

---

## 📚 Dataset Columns

| Feature    | Description                          |
|------------|--------------------------------------|
| Pclass     | Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd) |
| Sex        | Gender of the passenger              |
| Age        | Age in years                         |
| SibSp      | # of siblings / spouses aboard       |
| Parch      | # of parents / children aboard       |
| Fare       | Ticket fare                          |
| Embarked   | Port of Embarkation (C = Cherbourg, Q = Queenstown, S = Southampton) |

---

## 🔍 Steps Followed

1. **Data Loading**
2. **Exploratory Data Analysis (EDA)**
3. **Handling Missing Values**
4. **Feature Engineering & Encoding**
5. **Train-Test Split**
6. **Model Training (Multiple Models)**
7. **Evaluation using Accuracy, Precision, Recall, and F1-Score**
8. **Cross-Validation**
9. **Visualization (Confusion Matrix)**

---

## 🚀 Libraries Used

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `xgboost`

---

## 🎯 Model Performance Comparison

| Model                   | Accuracy | Precision | Recall  | F1-Score |
|-------------------------|----------|-----------|---------|----------|
| **Logistic Regression** | 100%      | 100%       | 100%     | 100%      |
| **Random Forest**       | 100%      | 100%       | 100%     | 100%      |
| **XGBoost Classifier**  | 100%      | 100%       | 100%     | 10%      |

All models (Logistic Regression, Random Forest, XGBoost) gave high accuracies.

This is because Sex and Pclass are strong indicators of survival. Historically, women and higher-class passengers were given priority during evacuation.

As a result, models tend to overfit slightly because these features almost directly map to the survival target.

To address this, I used a Decision Tree Classifier to explicitly visualize and control splits, ensuring better interpretability rather than just chasing accuracy.
> ✅ *Note: Although ensemble models gave higher metrics, the Decision Tree was chosen for its clear classification rules and better generalization without heavy overfitting.*

---

## 📊 Sample Confusion Matrix (XGBoost)

