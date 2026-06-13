# Loan Prediction Using Machine Learning

## Project Overview

This project aims to predict whether a loan application will be approved based on applicant information such as income, education level, employment status, property area, and credit history.

The project demonstrates a complete machine learning workflow including:

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Feature Selection
- Model Building
- Model Evaluation
- Model Comparison

---

## Dataset Information

The dataset contains 614 loan applications and 13 features.

### Features

| Feature | Description |
|----------|----------|
| Loan_ID | Unique Loan Identifier |
| Gender | Applicant Gender |
| Married | Marital Status |
| Dependents | Number of Dependents |
| Education | Education Level |
| Self_Employed | Self Employment Status |
| ApplicantIncome | Applicant Income |
| CoapplicantIncome | Co-applicant Income |
| LoanAmount | Loan Amount Requested |
| Loan_Amount_Term | Loan Repayment Term |
| Credit_History | Credit History Status |
| Property_Area | Urban, Semiurban, Rural |
| Loan_Status | Loan Approval Status (Target Variable) |

---

## Project Workflow

### 1. Data Understanding

- Dataset inspection
- Data type analysis
- Missing value analysis
- Statistical summary

### 2. Data Cleaning

#### Missing Value Treatment

Categorical Features:
- Imputed using Mode

Numerical Features:
- Imputed using Median

Reason:
- Median is robust to outliers.
- Mode preserves category distribution.

### 3. Exploratory Data Analysis (EDA)

Performed:

- Target Distribution Analysis
- Histograms
- Boxplots
- Correlation Heatmap
- Categorical Feature Analysis
- Outlier Detection

### 4. Feature Engineering

- Removed Loan_ID
- Encoded categorical variables
- Encoded target variable:
  - Y → 1
  - N → 0

### 5. Feature Selection

Chi-Square Test was used to assess feature relevance.

Key predictors identified:

- Credit_History
- ApplicantIncome
- CoapplicantIncome
- LoanAmount

### 6. Train-Test Split

- 80% Training Data
- 20% Testing Data
- Stratified Sampling used to preserve class distribution

### 7. Model Building

The following machine learning models were implemented:

#### Logistic Regression

Used as a baseline model with feature scaling.

#### Decision Tree Classifier

Used to capture non-linear decision boundaries.

#### Random Forest Classifier

Used to improve generalization through ensemble learning.

---

## Model Evaluation

Evaluation metrics used:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC Score
- 5-Fold Cross Validation

### Model Comparison

| Model | CV Score | Accuracy | Precision | Recall | F1 Score | ROC AUC |
|---------|---------|---------|---------|---------|---------|---------|
| Logistic Regression | 79.63% | **86.18%** | 84.00% | **98.82%** | **90.81%** | **0.802** |
| Decision Tree | 68.84% | 76.42% | 82.56% | 83.53% | 83.04% | 0.720 |
| Random Forest | 77.60% | 82.93% | **84.78%** | 91.76% | 88.14% | 0.796 |

---

## Key Insights

- Credit_History was the most important feature influencing loan approval.
- Income-related features showed strong predictive power.
- Logistic Regression outperformed Decision Tree and Random Forest on this dataset.
- High Recall indicates that approved loan applications were identified effectively.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## Project Structure

Loan_Prediction/

├── Loan_Prediction.ipynb

├── Loan_Prediction_Cleaned.csv

├── Model_Comparison.csv

├── Images/

│   ├── Missing_Values.png

│   ├── Correlation_Heatmap.png

│   ├── ROC_Curve_Logistic Regression.png

│   ├── ROC_Curve_Decision Tree.png

│   ├── ROC_Curve_Random Forest.png

│   ├── Confusion_Matrix_Logistic Regression.png

│   ├── Confusion_Matrix_Decision Tree.png

│   ├── Confusion_Matrix_Random Forest.png

│   └── Feature_Importance.png

├── README.md

└── requirements.txt

---

## Future Improvements

- Hyperparameter tuning using GridSearchCV
- XGBoost implementation
- Model deployment using Streamlit
- Real-time loan approval prediction application

---

## Author

Albin Karintholil Robert

MSc Data Science and Analytics (Distinction)

Aspiring Data Scientist | Machine Learning Enthusiast