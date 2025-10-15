## - Name : Mohd Fuzail 
## - Roll no.: CH22B080
## - Date :15-10-25


# 🧩 DA5401 A6 — Imputation via Regression for Missing Data

## 📘 Overview
This project explores different strategies to handle **missing data** and examines their effect on model performance.  
Using the **UCI Credit Card Default Clients Dataset**, missing values are artificially introduced to simulate a **Missing At Random (MAR)** scenario.  
The aim is to compare simple and regression-based imputations and evaluate their influence on a classification model.

---

## 🎯 Objectives
- Apply **Linear** and **Non-Linear Regression** techniques to impute missing values.  
- Compare regression-based imputation with **Median Imputation** and **Listwise Deletion**.  
- Evaluate the effect of each method using a **Logistic Regression classifier**.  

---

## 🧠 Methods Implemented

### 1. Data Preparation
- Loaded the UCI Credit Card Default dataset.  
- Introduced **5% missing values** in `AGE` and `BILL_AMT1` columns.  

### 2. Imputation Strategies
- **Dataset A – Median Imputation:**  
  Replaced missing values with the column median (robust to outliers).  
- **Dataset B – Linear Regression Imputation:**  
  Predicted missing `AGE` values using a Linear Regression model.  
- **Dataset C – Non-Linear Regression Imputation:**  
  Used **K-Nearest Neighbors (KNN) Regression** to predict missing `AGE` values.  
- **Dataset D – Listwise Deletion:**  
  Dropped all rows containing missing data.

### 3. Model Training and Evaluation
- Standardized features using `StandardScaler`.  
- Trained a **Logistic Regression** classifier on each dataset.  
- Evaluated performance using **Accuracy**, **Precision**, **Recall**, and **F1-score**.

---

## 📊 Results Summary
| Dataset | Imputation Method           | Accuracy   | Precision (Weighted) | Recall (Weighted) | F1-Score (Weighted) |
| ------- | --------------------------- | ---------- | -------------------- | ----------------- | ------------------- |
| A       | Median Imputation           | **0.7792** | **0.7832**           | **0.7792**        | **0.7811**          |
| B       | Linear Regression           | **0.7792** | **0.7832**           | **0.7792**        | **0.7811**          |
| C       | Non-Linear Regression (KNN) | **0.7792** | **0.7832**           | **0.7792**        | **0.7811**          |
| D       | Listwise Deletion           | **0.7805** | **0.7811**           | **0.7805**        | **0.7808**          |


---

## 💡 Key Insights
- The **median** is robust to outliers and suitable for skewed data.  
- **Regression-based imputations** preserve relationships among features.  
- **Listwise deletion** reduces data size and may degrade model performance.  
- **KNN imputation** captures non-linear patterns better when sufficient data is available.

---

## 🛠️ Technologies Used
- Python 3  
- Pandas, NumPy  
- Scikit-learn  
- Matplotlib, Seaborn  
- Jupyter Notebook / Google Colab  

---

## 🚀 How to Run
1. Clone the repository:  
   ```bash
   git clone https://github.com/Fuzail1929/DA5401_Assignment_6.git
   cd DA5401_Assignment_6
