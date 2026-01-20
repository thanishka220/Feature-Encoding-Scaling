# Task 4: Feature Encoding & Scaling – Adult Income Dataset

## 📌 Project Overview
This project focuses on preparing the **Adult Income Dataset** for Machine Learning by applying proper **feature encoding** and **feature scaling** techniques. The goal is to convert raw categorical and numerical data into an ML-ready format and understand the impact of scaling on model performance.

---

## 📂 Dataset Information
- **Dataset Name:** Adult Income Dataset
- **Source:** Kaggle  
- **Link:** https://www.kaggle.com/datasets/wenruliu/adult-income-dataset
- **Records:** 48,842 rows
- **Target Variable:** `income`

---

## 🛠️ Tools & Technologies Used
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  

---

## 📊 Feature Identification

### 🔹 Categorical Features
- workclass  
- education  
- marital-status  
- occupation  
- relationship  
- race  
- gender  
- native-country  
- income (target)

### 🔹 Numerical Features
- age  
- fnlwgt  
- educational-num  
- capital-gain  
- capital-loss  
- hours-per-week  

---

## 🔄 Data Preprocessing Steps

### 1️⃣ Handling Missing Values
- Replaced `?` with NaN
- Removed rows with missing values

### 2️⃣ Feature Encoding
- **Label Encoding** applied to the target variable `income`
  - `<=50K → 0`
  - `>50K → 1`
- **One-Hot Encoding** applied to nominal categorical features using `pd.get_dummies()`
- `drop_first=True` used to avoid multicollinearity

### 3️⃣ Feature Scaling
- **StandardScaler** applied to numerical features
- Transformed data to:
  - Mean ≈ 0
  - Standard Deviation ≈ 1

---

## 📈 Before vs After Scaling

### 🔹 Before Scaling
- Numerical features had different ranges
- Large values dominated distance-based models
- Slower convergence for gradient-based algorithms

### 🔹 After Scaling
- All numerical features standardized
- Improved model stability and performance
- Suitable for algorithms like KNN, SVM, Logistic Regression, and Neural Networks

---

## 🧠 Impact of Scaling on ML Algorithms

### ✅ Scaling is Important For:
- Logistic Regression
- KNN
- SVM
- Neural Networks
- Gradient Descent-based models

### ❌ Scaling Not Mandatory For:
- Decision Trees
- Random Forest
- XGBoost

---

## 📁 Project Files
- `feature encoding.ipynb` – Complete preprocessing notebook  
- `adult_income_preprocessed.zip` – Final processed dataset 

---

## ✅ Final Outcome
- Dataset converted to fully numerical format
- Features properly encoded and scaled
- ML-ready dataset created
- Clear understanding of preprocessing impact on machine learning models

---

## 📌 Conclusion
Feature encoding and scaling are crucial preprocessing steps in any machine learning pipeline. This project demonstrates how proper preprocessing improves data quality and model readiness while ensuring fairness across features.
