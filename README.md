# covid-mortality-predictor

# 🧠 COVID-19 Mortality Rate Predictor

This project builds a machine learning model to predict the **likelihood of death** in COVID-19 patients using anonymized data from the Mexican Government. It combines domain-relevant comorbidities and demographics with model explainability using SHAP.

---

## 🔍 Problem Statement

Accurate mortality prediction can help hospitals prioritize resources for high-risk COVID-19 patients. The objective is to classify patients as "deceased" or "recovered" based on initial hospital data.

---

## 📊 Features

| Feature Group | Example Fields |
|---------------|----------------|
| Demographics  | Age, Sex, Pregnancy |
| Comorbidities | Diabetes, Obesity, COPD, Renal issues |
| Hospital Info | ICU, Intubated, Pneumonia |
| COVID Test    | Classification Final |

---

## 🛠️ Tech Stack

- Python (pandas, scikit-learn, XGBoost)
- Imbalanced-learn (SMOTE)
- SHAP for model explainability
- Matplotlib / Seaborn for EDA

---

## 🔧 Model Pipeline

1. **EDA & Cleaning**
2. **Feature Engineering**
3. **Train-Test Split**
4. **SMOTE for Class Imbalance**
5. **Random Forest + XGBoost with GridSearchCV**
6. **SHAP Explainability**

---

## 📈 Results

- **Best Model**: XGBoost with SMOTE
- **ROC AUC**: 0.93
- **Recall (death)**: 0.91
- **Precision (death)**: 0.49

Confusion Matrix:

|               | Pred: No Death | Pred: Death |
|---------------|----------------|-------------|
| **Actual: No Death** | 57326         | 10223      |
| **Actual: Death**    | 982           | 9865       |

---

## 🎯 SHAP Feature Importance

![SHAP](images/summary_plot.png)

- Key predictors: Age, Pneumonia, ICU Admission, Renal Disease, Intubation

---

## 🚀 Getting Started

```bash
git clone https://github.com/your-username/covid-mortality-predictor.git
cd covid-mortality-predictor
pip install -r requirements.txt
