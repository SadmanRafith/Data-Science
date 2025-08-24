# 📊 Loan Approval Data Science Project  

## 📌 Project Overview  
This project focuses on **data preprocessing and exploratory analysis** of a loan approval dataset.  
The main objective is to identify the key factors influencing loan approvals and prepare the dataset for predictive modeling.  

---

## 📊 Dataset Description  
- **Source**: Modified version of the [Loan Approval Classification Dataset (Kaggle)](https://www.kaggle.com/datasets/taweilo/loan-approval-classification-data)  
- **Instances**: 201  
- **Features**: 13 attributes + 1 target (`loan_status`)  

**Target Variable**  
- `0` → Rejected  
- `1` → Accepted  

**Key Features**  
- `person_age` → Applicant’s age  
- `person_gender` → Gender (male, female)  
- `person_education` → Education level (High School, Bachelor, Master, etc.)  
- `person_income` → Annual income  
- `person_emp_exp` → Employment experience (years)  
- `person_home_ownership` → Home ownership (MORTGAGE, OWN, RENT, OTHER)  
- `loan_amnt` → Loan amount requested  
- `loan_intent` → Purpose of loan (Education, Medical, Personal, etc.)  
- `loan_int_rate` → Loan interest rate  
- `loan_percent_income` → Loan amount as % of annual income  
- `credit_score` → Applicant’s credit score  
- `cb_person_cred_hist_length` → Length of credit history  
- `previous_loan_defaults_on_file` → Previous loan defaults (Yes/No)  

---

## ❓ Primary Questions Explored  
- What demographic and financial factors influence loan approval/rejection?  
- How do categorical features (education, gender, home ownership) impact approval rates?  
- What correlations exist among numeric features (income, loan amount, credit score, etc.)?  
- How can missing values, outliers, and class imbalance be effectively handled?  
- Does preprocessing improve dataset reliability for modeling?  

---

## 🔧 Workflow  

### 🔹 Data Preprocessing  
- Removed duplicates  
- Fixed invalid categorical values (using string similarity)  
- Converted categorical text to lowercase  
- Label encoding for categorical features  

### 🔹 Handling Missing Values  
- Techniques used:  
  - Top-down & Bottom-up imputation  
  - Mode (categorical)  
  - Median (numeric – due to skewness & outliers)  

### 🔹 Outlier Detection & Treatment  
- Z-score method (|z| > 3)  
- IQR method (Q1–1.5×IQR, Q3+1.5×IQR)  

### 🔹 Class Imbalance Handling  
- **Upsampling** → Increased minority class instances  
- **Downsampling** → Reduced majority class instances  

### 🔹 Feature Scaling & Transformation  
- Normalization (Min-Max scaling)  
- Chi-Square based binning of numeric features  

### 🔹 Visualization & Analysis  
- Distribution plots for categorical & numeric variables  
- Missing values visualization  
- Correlation matrix (`corrplot`)  

### 🔹 Exporting Final Dataset  
- Preprocessed dataset saved as: `data_preprocessed.xlsx`  

---

## ✅ Findings  
- Strong predictors of loan approval: **credit score, income, loan amount, loan percent income**  
- Categorical factors like **education** and **home ownership** impact approval likelihood  
- Correlation analysis revealed strong relationships between numeric features  
- Preprocessing improved dataset balance and reduced skewness  

---

## ⚠️ Limitations  
- Small dataset size (**201 instances**) limits generalizability  
- Imputation (mode/median) may introduce bias  
- Downsampling caused some information loss  

---

## 🚀 Next Steps  
- Apply machine learning models (Logistic Regression, Decision Trees, Random Forest, etc.)  
- Compare results with different preprocessing strategies  
- Deploy a loan approval prediction system  

---

## 📂 Project Structure (Recommended)  
