# 🫀 Cardiovascular Disease Prediction Using Machine Learning

This project focuses on building a machine learning system to predict the likelihood of cardiovascular disease using patient medical records and lifestyle information. The workflow includes data preprocessing, feature engineering, exploratory data analysis (EDA), model training, hyperparameter tuning, and evaluation.

---

## 📌 Project Overview

Cardiovascular diseases are one of the leading causes of death worldwide. Early prediction can help in prevention and timely medical intervention. This project uses multiple machine learning models to classify whether a patient is at risk of heart disease.

---

## 📊 Dataset Description

The dataset contains **70,000 patient records** with the following attributes:

### 🧍 Demographic Features
- Age
- Gender
- Height
- Weight

### 🩺 Medical Measurements
- Systolic Blood Pressure (`ap_hi`)
- Diastolic Blood Pressure (`ap_lo`)
- Cholesterol Level
- Glucose Level

### 🧑‍⚕️ Lifestyle Factors
- Smoking
- Alcohol intake
- Physical activity

### 🎯 Target Variable
- `cardio` → Renamed as **Heart_Disease**
  - 0 → No disease
  - 1 → Disease present

---

## 🧪 Feature Engineering

To improve model performance, several new features were created:

- **BMI (Body Mass Index)**
- **Pulse Pressure**
- **Mean Arterial Pressure**
- **Blood Pressure Ratio**
- **Risk Score** (based on lifestyle + medical indicators)
- **Hypertension Flag**
- **Age Groups**
- **BMI Categories**
- **Interaction Features**:
  - Age × BMI
  - Age × Blood Pressure

---

## 🧹 Data Preprocessing

The dataset was cleaned and prepared using the following steps:

- Removal of invalid blood pressure values
- Filtering unrealistic height, weight, and BMI values
- Conversion of age from days → years
- Handling infinite and missing values
- Encoding categorical variables
- Feature scaling using `StandardScaler`

---

## 📈 Exploratory Data Analysis (EDA)

The following visualizations were used to understand the dataset:

- Distribution plots (BMI, age, etc.)
- Box plots (outlier detection)
- Count plots (class imbalance analysis)
- Pair plots (feature relationships)
- Correlation heatmap
- Group comparisons (heart disease vs features)

---

## 🤖 Machine Learning Models Used

The following models were trained and optimized using GridSearchCV:

### 1. Logistic Regression
- Baseline linear model
- Class balancing applied

### 2. Random Forest Classifier
- Ensemble learning method
- Captures nonlinear relationships

### 3. XGBoost Classifier
- Gradient boosting framework
- High performance on structured data

### 4. LightGBM Classifier
- Fast and efficient gradient boosting model
- Handles large datasets effectively

---

## ⚙️ Hyperparameter Tuning

GridSearchCV was used to optimize each model:

- Logistic Regression: C, solver
- Random Forest: n_estimators, max_depth, min_samples_split, min_samples_leaf
- XGBoost: learning_rate, max_depth, subsample, n_estimators
- LightGBM: num_leaves, learning_rate, max_depth, n_estimators

---

## 📊 Model Evaluation Metrics

Models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC Score

Additionally:
- Confusion Matrix
- ROC Curves
- Feature Importance Analysis

---

## 🏆 Results Summary

All models performed competitively with similar accuracy (~73%).  
The best model was selected based on **ROC-AUC score and balanced performance**.

| Model               | Performance Summary |
|--------------------|--------------------|
| Logistic Regression | Strong baseline     |
| Random Forest       | Stable performance  |
| XGBoost             | High predictive power |
| LightGBM            | Best overall balance |

---

## 📌 Feature Importance Insights

Key factors influencing heart disease prediction:

- Blood pressure (ap_hi, ap_lo)
- Age
- BMI
- Cholesterol level
- Glucose level
- Physical activity

---

## 📉 Visual Outputs

The project includes:

- ROC Curves comparison
- Confusion matrices for all models
- Feature importance plots
- Pair plots and correlation heatmaps

---

## 🚀 How to Run the Project

### 1. Clone the repository
```bash
git clone https://github.com/your-username/cardiovascular-disease-prediction.git
cd cardiovascular-disease-prediction
