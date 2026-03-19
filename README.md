# Loan Default Risk Prediction

## Project Overview

This project builds a machine learning model to predict whether a customer is likely to default on a loan.
It covers the complete ML pipeline from data preprocessing to model evaluation and hyperparameter tuning.

The objective is to help financial institutions identify high-risk customers and make better lending decisions.

---

## Dataset

The dataset contains customer financial and demographic details such as:

* Age, Income, Savings
* Monthly Expenses
* Credit Score
* Loan Amount & Loan Term
* Employment Years
* Home Ownership
* Education
* Marital Status
* Region
* Recent Default History

### Target Variable

`target_default_risk`

* **0** → No Default
* **1** → Default

---

## Project Workflow

### 1. Data Cleaning

* Handled missing values using **median imputation**
* Fixed categorical inconsistencies (e.g., spelling issues)
* Removed irrelevant columns like `customer_id`

---

### 2. Exploratory Data Analysis (EDA)

* Value counts and countplots for categorical features
* Distribution analysis of numerical features
* Correlation heatmap
* Outlier detection using boxplots

---

### 3. Feature Engineering

Created new meaningful features:

* `income_per_dependent`
* `savings_to_income_ratio`

These features help capture **financial pressure and stability**.

---

### 4. Data Preprocessing

* Train-test split (80-20)
* **Ordinal Encoding** for education
* **One-Hot Encoding** for categorical variables
* **StandardScaler** for numerical features
* Outlier treatment using **IQR-based capping (Winsorization)**

---

### 5. Models Implemented

The following models were trained and evaluated:

* Logistic Regression
* Decision Tree
* Support Vector Machine (SVM)
* Random Forest
* XGBoost

---

### 6. Hyperparameter Tuning

* Used **RandomizedSearchCV** and **GridSearchCV**
* Focused on improving:

  * Random Forest
  * XGBoost

---

### 7. Evaluation Metrics

Models were evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix

---

## Results

* Random Forest and XGBoost performed the best
* XGBoost achieved the highest accuracy after tuning
* Feature engineering significantly improved model performance

---

## Technologies Used

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Scikit-learn
* XGBoost
* Jupyter Notebook

---

## How to Run

1. Clone the repository

```
git clone https://github.com/prabandkumar/loan-default-risk-prediction.git
```

2. Install dependencies

```
pip install -r requirements.txt
```

3. Run the notebook

```
jupyter notebook
```

---

## Future Improvements

* Build a web app using Flask or FastAPI
* Add model explainability (SHAP values)
* Deploy model on cloud
* Improve feature engineering

---


