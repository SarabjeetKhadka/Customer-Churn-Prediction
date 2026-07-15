# Customer-Churn-Prediction  (ML)

# Customer Churn Prediction Using Machine Learning

## 1. Project Overview

Customer retention is one of the most important factors influencing the long-term success of a business. Acquiring new customers is often more expensive than retaining existing ones, making customer churn prediction a valuable business application.

This project develops machine learning models to predict whether a customer is likely to leave a telecommunications company based on demographic information, service subscriptions, account details, and billing information.

The project follows a complete machine learning workflow, including data exploration, preprocessing, model development, evaluation, and business interpretation of results.

---

## 2. Problem Statement

Telecommunication companies face significant revenue loss when customers discontinue their services. Identifying customers who are likely to churn allows businesses to take proactive actions and improve customer retention.

The challenge is to build a predictive model that can accurately identify customers at risk of churn using historical customer data.

---

## 3. Objective

The primary objectives of this project are:

* Analyze customer data and identify factors related to churn.
* Perform data preprocessing and feature engineering.
* Build multiple machine learning classification models.
* Compare model performance using standard evaluation metrics.
* Identify the most effective model for churn prediction.
* Generate business insights that support customer retention strategies.

---

## 4. Dataset Description

### Dataset

Telco Customer Churn Dataset

### File

WA_Fn-UseC_-Telco-Customer-Churn.csv

### Dataset Contents

The dataset contains information about:

* Customer demographics
* Service subscriptions
* Internet services
* Account information
* Billing details
* Customer churn status

### Target Variable

**Churn**

Target Encoding:

* No → 0
* Yes → 1

A value of 1 indicates that the customer left the company, while 0 indicates the customer remained.

---

## 5. Features Used

The dataset includes several customer-related attributes such as:

### Demographic Features

* gender
* SeniorCitizen
* Partner
* Dependents

### Service Features

* PhoneService
* MultipleLines
* InternetService
* OnlineSecurity
* OnlineBackup
* DeviceProtection
* TechSupport
* StreamingTV
* StreamingMovies

### Account Features

* tenure
* Contract
* PaperlessBilling
* PaymentMethod

### Billing Features

* MonthlyCharges
* TotalCharges

### Excluded Feature

* customerID

Reason:

CustomerID is a unique identifier and does not contain predictive information for machine learning models.

---

## 6. Technologies Used

### Programming Language

* Python

### Libraries

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

### Development Environment

* Jupyter Notebook
* Google Colab (Optional)

---

## 7. Machine Learning Workflow

The project follows the following workflow:

1. Data Loading
2. Exploratory Data Analysis (EDA)
3. Missing Value Analysis
4. Duplicate Record Check
5. Data Preprocessing
6. Feature Encoding
7. Train-Test Split
8. Model Training
9. Model Evaluation
10. ROC-AUC Analysis
11. Feature Importance Analysis
12. Model Comparison
13. Business Recommendations

---

## 8. Exploratory Data Analysis

The exploratory analysis focuses on understanding customer behavior and identifying potential factors associated with churn.

The following analyses are performed:

* Dataset structure inspection
* Missing value analysis
* Duplicate record analysis
* CustomerID uniqueness verification
* Churn distribution analysis
* Contract type vs churn
* Monthly charges vs churn
* Tenure distribution
* Internet service analysis

### Key EDA Findings

* Customers with month-to-month contracts tend to churn more frequently.
* Customers with shorter tenure show higher churn rates.
* Monthly charges may influence customer retention behavior.
* Service-related features contribute significantly to customer decisions.

---

## 9. Data Preprocessing

The following preprocessing steps are applied before model training.

### CustomerID Handling

* Verified uniqueness of customerID.
* Removed customerID from the feature set.

### TotalCharges Conversion

* Converted TotalCharges from object datatype to numerical datatype using:

```python id="e6vvwy"
pd.to_numeric(errors='coerce')
```

* Missing values generated during conversion were identified.
* Rows containing missing TotalCharges values were removed.

### Target Encoding

Churn values were converted to numerical format:

* No → 0
* Yes → 1

### Categorical Feature Encoding

One-Hot Encoding was applied to transform categorical variables into machine-readable numerical features.

---

## 10. Models Implemented

### Logistic Regression

Purpose:

* Baseline classification model
* Estimates churn probability

### Decision Tree Classifier

Purpose:

* Captures non-linear relationships
* Generates interpretable decision rules

### Random Forest Classifier

Purpose:

* Ensemble learning approach
* Improves predictive performance and generalization

---

## 11. Evaluation Metrics

The following metrics are used to evaluate model performance.

### Accuracy

Measures the percentage of correctly classified observations.

### Precision

Measures how many predicted churn customers actually churned.

### Recall

Measures how many actual churn customers were successfully identified.

### F1-Score

Provides a balance between precision and recall.

### ROC-AUC

Measures the model's ability to distinguish between churn and non-churn customers across different thresholds.

---

## 12. Results

Each machine learning model is evaluated on unseen test data.

Performance metrics include:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC

Confusion matrices and ROC curves are used to visualize performance and compare model effectiveness.

---

## 13. Model Comparison

The final comparison is performed using:

| Model               | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
| ------------------- | -------- | --------- | ------ | -------- | ------- |
| Logistic Regression | TBD      | TBD       | TBD    | TBD      | TBD     |
| Decision Tree       | TBD      | TBD       | TBD    | TBD      | TBD     |
| Random Forest       | TBD      | TBD       | TBD    | TBD      | TBD     |

The model achieving the strongest balance of performance metrics will be selected as the best-performing model.

---

## 14. Key Findings

The analysis aims to identify customer characteristics associated with churn.

Potential findings include:

* Contract type influences customer retention.
* Customer tenure impacts churn probability.
* Billing patterns contribute to churn behavior.
* Service subscriptions affect customer loyalty.

Feature Importance Analysis is used to identify the most influential predictors.

---

## 15. Business Recommendations

Based on the findings, organizations can:

* Identify customers at high risk of churn.
* Implement targeted retention campaigns.
* Encourage long-term contract adoption.
* Improve customer engagement strategies.
* Reduce revenue loss caused by customer attrition.

Using predictive analytics enables businesses to make proactive and data-driven decisions.

---

## 16. Conclusion

This project demonstrates the application of supervised machine learning techniques for customer churn prediction.

By comparing Logistic Regression, Decision Tree, and Random Forest classifiers, the project identifies the most effective model for predicting customer churn.

The insights generated through exploratory data analysis, feature importance evaluation, and model comparison can help organizations improve customer retention and support strategic decision-making.

Customer churn prediction serves as a practical example of how machine learning can create measurable business value through proactive customer management.


## NOTE FOR PROJECT STRUCTURE

Section 1:

Project Introduction

Section 2:

Import Required Libraries

Section 3:

Load Dataset

Section 4:

Exploratory Data Analysis

Section 5:

Data Preprocessing

Section 6:

Feature & Target Separation

Section 7:

Train-Test Split

Section 8:

Model Training

Section 9:

Model Evaluation

Section 10:

Confusion Matrix Analysis

Section 11:

ROC Curve & AUC Analysis

Section 12:

Feature Importance Analysis

Section 13:

Final Model Comparison

Section 14:

Conclusion
