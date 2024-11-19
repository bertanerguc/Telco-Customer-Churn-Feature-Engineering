# 🌟 Telco Customer Churn Feature Engineering

This project aims to predict customer churn for a telecom company by developing a **machine learning model**. The focus is on performing **exploratory data analysis (EDA)** and **feature engineering** to improve the model's performance.

---

## 🚀 Project Overview

### 📝 Problem Statement
The goal is to predict which customers are likely to leave the telecom service (`Churn = Yes`) based on their account information, demographics, and services used. An accurate model can help the company retain customers by identifying and addressing the reasons for churn.

### 📊 Dataset
The dataset contains information about **7,043 customers** from a fictional telecom company in California. Each row represents a unique customer, including details about their services, account, and demographic information.

---

## 📂 Dataset Features

| Feature              | Description                                                       |
|----------------------|-------------------------------------------------------------------|
| `CustomerId`         | Unique customer identifier                                       |
| `Gender`             | Gender of the customer                                           |
| `SeniorCitizen`      | Whether the customer is a senior citizen (1 = Yes, 0 = No)       |
| `Partner`            | Whether the customer has a partner (Yes/No)                      |
| `Dependents`         | Whether the customer has dependents (Yes/No)                     |
| `Tenure`             | Number of months the customer has stayed with the company        |
| `PhoneService`       | Whether the customer has phone service (Yes/No)                  |
| `InternetService`    | Type of internet service (DSL/Fiber optic/No)                    |
| `MonthlyCharges`     | The amount charged to the customer monthly                       |
| `TotalCharges`       | The total amount charged to the customer                         |
| `Churn`              | Whether the customer has churned (Yes/No)                        |

---

## 🔧 Key Features

### 🛠 Tasks

1. **Exploratory Data Analysis (EDA)**:
   - Analyze numerical and categorical variables.
   - Identify missing and outlier values.
   - Investigate correlations and relationships with the target variable (`Churn`).
2. **Feature Engineering**:
   - Handle missing and outlier values.
   - Create new meaningful features to enhance the dataset.
   - Encode categorical variables for model compatibility.
3. **Model Building**:
   - Train a machine learning model using the processed dataset.
   - Evaluate the model's performance with metrics like accuracy, precision, recall, F1 score, and AUC.

---

## 📈 Project Workflow

### 1️⃣ Exploratory Data Analysis (EDA)
- **Analyze Features**: 
  - Separate categorical and numerical variables.
  - Examine target variable (`Churn`) distribution.
- **Handle Missing Values**:
  - Impute missing values in `TotalCharges` using the median.
- **Outlier Detection**:
  - Identify and cap outliers for numerical variables using IQR thresholds.

### 2️⃣ Feature Engineering
- Create new features, such as:
  - `NEW_TENURE_YEAR`: Categorize tenure into yearly groups.
  - `NEW_Engaged`: Flag customers with long-term contracts.
  - `NEW_TotalServices`: Count the total number of services a customer uses.
  - `NEW_AVG_Service_Fee`: Calculate the average service fee per service.
- Encode categorical variables using **Label Encoding** and **One-Hot Encoding**.

### 3️⃣ Model Building
- Split the dataset into training and testing sets.
- Train a **CatBoostClassifier** model for churn prediction.
- Evaluate performance using metrics:
  - Accuracy: 80%
  - Recall: 66%
  - Precision: 51%
  - F1 Score: 58%
  - AUC: 75%

---

## 📊 Results

### 🎯 Key Insights

1. **Significant Predictors**:
   - Long-term contracts and monthly charges are key factors affecting churn.
   - Customers with higher total services are less likely to churn.
2. **Performance Metrics**:
   - **Baseline Accuracy**: 78.4%
   - **Final Model Accuracy**: 80%
   - Significant improvements were observed in recall and F1 score after feature engineering.

---

## 🛠 Tools and Libraries

- **Python**  
- **Pandas**  
- **NumPy**  
- **Scikit-learn**  
- **CatBoost**  
- **Seaborn**  
- **Matplotlib**  

---

## 🌟 Contribution

Contributions are welcome!  
Feel free to fork this repository, create issues, or submit pull requests for improvements.

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).
