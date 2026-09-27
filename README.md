# CODSOFT TASK 3 - Customer Churn Prediction

## 👥 Project Overview

This project focuses on predicting customer churn for a subscription-based service using Machine Learning.

The model predicts whether a customer is likely to:

- **Stay** with the company
- **Churn** and leave the company

## 🎯 Objective

To develop a Machine Learning model that can predict customer churn using historical customer information such as credit score, age, balance, tenure, activity status, and other customer attributes.

## 🛠️ Technologies Used

- Python
- Pandas
- Scikit-learn
- Matplotlib
- Logistic Regression
- Random Forest
- Joblib
- Google Colab

## 📊 Dataset

The dataset contains customer information and a target column called `Exited`.

The `Exited` column represents customer churn:

- `0` = Customer stayed
- `1` = Customer churned

The dataset contains **10,000 customer records**.

## 🔄 Project Workflow

Dataset  
↓  
Data Cleaning  
↓  
Remove Unnecessary Columns  
↓  
Categorical Feature Encoding  
↓  
Train-Test Split  
↓  
Feature Scaling  
↓  
Logistic Regression  
↓  
Random Forest  
↓  
Model Evaluation  
↓  
Customer Churn Prediction

## 🧹 Data Preprocessing

The following identifier columns were removed because they are not useful for predicting churn:

- `RowNumber`
- `CustomerId`
- `Surname`

Categorical features such as:

- `Geography`
- `Gender`

were converted into numerical features using one-hot encoding.

Numerical features were scaled for Logistic Regression using `StandardScaler`.

## 🤖 Machine Learning Models

### Logistic Regression

Logistic Regression was used as a baseline classification model for predicting whether a customer would churn.

### Random Forest

A Random Forest Classifier was also trained to capture more complex relationships between customer features and churn behavior.

The two models were evaluated and compared based on their performance.

## 📈 Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

A model comparison graph was also created to compare the accuracy of Logistic Regression and Random Forest.

## 🧪 Custom Customer Prediction

The trained Random Forest model was tested with a new customer profile.

The system predicts whether the customer is likely to:

- ✅ Stay
- ⚠️ Churn

The model can also provide an estimated probability of churn.

## 💾 Model Saving

The trained Random Forest model and scaler were saved using Joblib:

```text
customer_churn_model.pkl
customer_churn_scaler.pkl
