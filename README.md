   # ML Lab Portfolio
   
   This repository contains my Machine Learning lab work and projects for the semester.


#1. Titanic Survival DatasetProblem Type: Binary Classification. 
#Target Variable: Survived (0 = No, 1 = Yes).
#Key Cleaning Challenges: Heavily missing data in the Cabin column, missing values in Age and Embarked, and non-numeric representations in identifiers.
#Cleaning Actions: Impute Age using the median (robust to outliers) , impute Embarked using the mode , drop the sparse Cabin column , remove duplicate records , and strip identifier columns like PassengerId, Name, and Ticket.


#2. Telco Customer Churn DatasetProblem Type: Binary Classification.
#Target Variable: Churn (Yes/No).
#Key Cleaning Challenges: Numeric values misrecorded as strings (e.g., blank strings in TotalCharges) and trailing/leading whitespaces in text.
#Cleaning Actions: Forcibly convert TotalCharges to numeric using pd.to_numeric(..., errors='coerce') to capture hidden blank strings as NaN values , fill or drop those missing rows , strip whitespace from text, and drop the customerID column to prevent overfitting.

#3. Student Performance DatasetProblem Type: Regression (predicting continuous exam scores) or Classification (if grouping scores into pass/fail bands).
#Target Variable: User's choice of individual subject scores (math, reading, writing) or a derived average score.
#Key Cleaning Challenges: The data is pre-cleaned with no missing entries or duplicates , making it a test for verification of data integrity.
#Cleaning Actions: Standardize string capitalization and spacing (convert to lowercase and strip whitespaces) , verify that types are correct integers, check for unexpected duplicates anyway, and separate the chosen target variable.

#4. Heart Disease Dataset (Cleveland Subset)Problem Type: Binary Classification.
#Target Variable: num or target (0 = no disease, 1 = presence of heart disease).
#Key Cleaning Challenges: Missing data represented as ? or blank spaces, categorical data stored awkwardly as numeric codes, and extreme medical outliers (e.g., cholesterol).
#Cleaning Actions: Load with na_values=["?"] to auto-detect missing elements , impute missing features like thal and ca using the mode , map cryptic numeric codes to descriptive text labels for clinical interpretability , check for impossible/negative values , and isolate the target feature. 
