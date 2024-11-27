# Customer Churn Prediction - End-to-End Data Science Pipeline

## Name: Rohan Devikoppa Shreedhara
## Z Number: Z23802492

## Project Overview
This project implements a comprehensive end-to-end data science pipeline to solve the **Customer Churn Prediction** problem. The goal is to predict whether a customer will churn (i.e., leave a service) based on various customer demographics and service usage attributes. 

The pipeline covers all stages of the data science process:
- **Exploratory Data Analysis (EDA)**
- **Data Preprocessing**
- **Feature Engineering**
- **Model Building and Evaluation**
- **Insights and Recommendations**

---

## Dataset
The dataset used for this project is the **Telecom Customer Churn Dataset** from Kaggle.  
- **Rows**: 7,043  
- **Columns**: 21  
- **Target Variable**: `Churn` (0 = Not Churn, 1 = Churn)

Key features:
- Customer demographics: `gender`, `SeniorCitizen`, `Partner`, `Dependents`
- Service details: `tenure`, `MonthlyCharges`, `TotalCharges`
- Subscription types: `InternetService`, `Contract`, `PaymentMethod`

---

## Pipeline Stages

### 1. Exploratory Data Analysis (EDA)
- **Techniques Used**:
  - Visualizations of feature distributions and the target variable using `matplotlib` and `seaborn`.
  - Correlation heatmap to identify relationships between numeric features.
  - Boxplots for outlier detection.
- **Insights**:
  - `Contract` and `tenure` significantly affect churn likelihood.
  - Customers with month-to-month contracts are more likely to churn.

---

### 2. Data Preprocessing
- **Steps**:
  - Imputation of missing values in numeric columns using mean values.
  - Encoding of categorical variables using `LabelEncoder`.
  - Feature scaling with `StandardScaler` for numeric attributes.
- **Outcome**:
  - Cleaned and normalized dataset ready for model training.

---

### 3. Feature Engineering
- **Dimensionality Reduction**: 
  - Applied Principal Component Analysis (PCA) to reduce the dataset to 5 components while retaining 95% of the variance.
- **Feature Selection**:
  - Recursive Feature Elimination (RFE) was used to select the most impactful features.

---

### 4. Model Building
- **Models Used**:
  - Logistic Regression
  - Random Forest Classifier
  - K-Means Clustering
- **Evaluation Metrics**:
  - Accuracy, Precision, Recall, F1-Score for classification models.
  - Silhouette Score for clustering.
- **Results**:
  - Logistic Regression: Accuracy = 81%, F1-Score for churn = 0.61.
  - Random Forest: Accuracy = 80%, F1-Score for churn = 0.57.
  - K-Means: Silhouette Score = 0.45.

---

### 5. Insights and Recommendations
- Customers with shorter tenures and month-to-month contracts are more likely to churn.
- Offering incentives like discounts or switching them to longer-term contracts may reduce churn.
- Improved identification of churners can enable targeted marketing campaigns.

---
