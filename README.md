# Credit Risk Predictor

A Machine Learning-powered web application that predicts whether a loan applicant is a **Good Credit Risk** or **Bad Credit Risk** based on demographic, financial, and banking information.

Built using **Python, Scikit-Learn, XGBoost, and Streamlit**.

---

# Project Overview

Credit risk assessment is a critical task for banks and financial institutions. Incorrect lending decisions can lead to significant financial losses.

This project develops and deploys a machine learning model capable of predicting the creditworthiness of applicants using historical credit data.

The final solution includes:

* Data preprocessing
* Exploratory Data Analysis (EDA)
* Feature engineering
* Hyperparameter tuning
* Model comparison
* Streamlit deployment
* Model and encoder persistence

---

# Problem Statement

Given information about a loan applicant such as:

* Age
* Job
* Housing status
* Savings account status
* Checking account status
* Credit amount
* Loan duration
* Purpose of loan

Predict whether the applicant represents:

* **Good Credit Risk**
* **Bad Credit Risk**

---

# Dataset Features

| Feature          | Description               |
| ---------------- | ------------------------- |
| Age              | Applicant age             |
| Sex              | Gender of applicant       |
| Job              | Employment category (0–3) |
| Housing          | Housing status            |
| Saving accounts  | Savings account category  |
| Checking account | Checking account category |
| Credit amount    | Requested loan amount     |
| Duration         | Loan duration in months   |
| Purpose          | Purpose of the loan       |

---

# Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* XGBoost
* Joblib
* Streamlit

---

# Machine Learning Workflow

## 1. Data Preprocessing

### Handling Categorical Features

The following categorical features were encoded:

* Sex
* Housing
* Saving accounts
* Checking account
* Purpose

LabelEncoder was used and the encoders were saved for deployment.

---

## 2. Exploratory Data Analysis

EDA was performed using:

* Count plots
* Box plots
* Violin plots
* Correlation heatmaps
* Distribution plots

Key analyses included:

* Risk distribution
* Credit amount patterns
* Loan duration patterns
* Housing and account status impact
* Purpose-based risk comparison

---

## 3. Train-Test Split

The dataset was split into:

```python
train_size = 80%
test_size = 20%
```

Using:

```python
train_test_split(
    X,
    y,
    test_size=0.2,
    stratify=y,
    random_state=1
)
```

---

## 4. Models Evaluated

### Decision Tree Classifier

Hyperparameters tuned:

* max_depth
* min_samples_split
* min_samples_leaf

---

### Random Forest Classifier

Hyperparameters tuned:

* n_estimators
* max_depth
* min_samples_split
* min_samples_leaf

---

### Extra Trees Classifier

Hyperparameters tuned:

* n_estimators
* max_depth
* min_samples_split
* min_samples_leaf

---

### XGBoost Classifier

Hyperparameters tuned:

* n_estimators
* learning_rate
* max_depth

---

## 5. Hyperparameter Tuning

GridSearchCV was used for automated hyperparameter optimization.

Example:

```python
GridSearchCV(
    estimator=model,
    param_grid=param_grid,
    cv=5,
    scoring="accuracy",
    n_jobs=-1
)
```

---

# Model Deployment

The best-performing model was saved using Joblib and integrated into a Streamlit application.

Saved files include:

```text
XGboost_credit_model.pkl
target_encoder.pkl

Sex_encoder.pkl
Housing_encoder.pkl
Saving accounts_encoder.pkl
Checking account_encoder.pkl
Purpose_encoder.pkl
```

---

# Project Structure

```text
Credit_Risk_Predictor/
│
├── credit_risk.ipynb
├── credit_model_app.py
├── dataset.xls
│
├── XGboost_credit_model.pkl
├── target_encoder.pkl
│
├── Sex_encoder.pkl
├── Housing_encoder.pkl
├── Saving accounts_encoder.pkl
├── Checking account_encoder.pkl
├── Purpose_encoder.pkl
│
└── README.md
```

---

# Installation

## Clone Repository

```bash
git clone https://github.com/puneethakshay00-cpu/Credit_Risk_Predictor.git

cd Credit_Risk_Predictor
```

---

## Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost streamlit joblib
```

---

# Running the Application

Launch the Streamlit app:

```bash
streamlit run credit_model_app.py
```

The application will open automatically in your browser.

---

# Using the Application

Enter:

* Age
* Sex
* Job category
* Housing status
* Saving account status
* Checking account status
* Credit amount
* Loan duration
* Purpose of loan

Click:

```text
Predict Risk
```

The model will display either:

```text
Low CREDIT RISK
```

or

```text
High CREDIT RISK
```

---

# Example Prediction

### Input

```text
Age: 35
Sex: Male
Job: 2
Housing: Own
Saving Accounts: Moderate
Checking Account: Little
Credit Amount: 5000
Duration: 24
Purpose: Car
```

### Output

```text
High CREDIT RISK
```

---

# Future Improvements

* Probability score prediction
* Model explainability using SHAP
* Feature importance visualization
* Docker deployment
* CI/CD pipeline
* Cloud deployment on AWS/GCP/Azure
* REST API integration

---

# Learning Outcomes

This project demonstrates:

* Data preprocessing
* Feature encoding
* Exploratory Data Analysis
* Classification algorithms
* Hyperparameter tuning
* Model persistence
* Streamlit deployment
* End-to-end Machine Learning workflow

---

# Author

**Puneeth Akshay**

GitHub: https://github.com/puneethakshay00-cpu

---

# License

This project is created for educational, research, and portfolio purposes.
# Credit_Risk_Predictor
