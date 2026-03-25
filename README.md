🏥 Healthcare Patient Risk Analysis
📌 Overview

This project is developed as part of an AI/ML assignment to analyze healthcare data and build a simple intelligent system for prediction and decision support.

The project combines data analysis, machine learning, anomaly detection, and a rule-based AI recommendation system to simulate real-world healthcare analytics.

🎯 Objectives

The main objectives of this project are:

- Perform exploratory data analysis (EDA) to understand patient data
- Build a machine learning model to predict patient test results
- Detect anomalies in billing amounts
- Generate AI-based doctor-style recommendations based on predictions

 📊 Dataset Description

The dataset contains patient-related information such as:

- Age, Gender, Blood Type
- Medical Condition
- Admission Type
- Billing Amount
- Medication
- Date of Admission & Discharge
- Test Results

Dataset Source:
Kaggle Healthcare Dataset

🔍 Approach

1. Data Preprocessing

- Removed irrelevant columns (Name, Doctor, Hospital)
- Converted date columns into **Stay Duration**
- Handled missing values
- Encoded categorical variables using one-hot encoding
- Converted target variable (`Test Results`) into numeric format

2. Exploratory Data Analysis (EDA)

EDA was performed to understand patterns and distributions in the data.
Key Insights:

- Majority of patients belong to a mid-age group
- Billing amounts show a right-skewed distribution (few high-cost cases)
- Certain medical conditions are more frequent
- Emergency admissions are relatively high
- Some medications are commonly prescribed
Visualizations Used:

- Histograms (Age, Billing Amount, Room Number)
- Count plots (Medical Condition, Admission Type, Medication)
- Boxplot for outlier detection

3. Supervised Learning

Objective:
Predict Test Results based on patient features

Model Used:
Random Forest Classifier

Steps:

- Split dataset into training and testing sets (80:20)
- Trained the model on training data
- Predicted results on test data

Evaluation Metrics:

- Accuracy Score
- Classification Report
- Confusion Matrix

Result:

The model achieved reasonable accuracy and was able to capture patterns in patient data effectively.

4. Anomaly Detection

Objective:
Identify unusual billing amounts

Method Used:
Z-score method

Observations:

- High billing anomalies may indicate:
  - Surgeries or ICU cases
  - Severe medical conditions
- Low billing anomalies may indicate:
  - Short stays
  - Minor treatments

These anomalies can be useful for auditing or identifying rare cases.

5. AI Doctor Recommendation Generator

A simple rule-based system was created to simulate doctor-like recommendations.

Input:

- Age
- Medical Condition
- Medication
- Predicted Test Result

Output:

- Structured medical recommendation
- Condition-based advice
- General health suggestions

#### Sample Output:
