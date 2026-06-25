# Heart Disease Prediction using Machine Learning

## Project Overview

This project applies Machine Learning techniques to predict whether a person is at risk of heart disease based on medical attributes. The model uses patient health data to classify whether heart disease is present or not.

Heart disease is one of the leading causes of death worldwide. Early prediction can help doctors make timely medical decisions and improve patient outcomes.

This project demonstrates data preprocessing, exploratory data analysis (EDA), binary classification, model evaluation, and feature importance analysis.

---

## Problem Statement

Build a classification model that predicts whether a patient has heart disease using medical data.

This is a binary classification problem:

* **0 → No Heart Disease**
* **1 → Heart Disease Present**

The model learns from historical patient records and predicts disease risk for unseen patients.

---

## Dataset

Dataset used: **Heart Disease UCI Dataset (Kaggle)**

The dataset contains medical and diagnostic information about patients.

### Features

* **age** — Age of patient
* **sex** — Gender
* **chest_pain_type** — Type of chest pain
* **resting_blood_pressure** — Resting blood pressure
* **cholestoral** — Cholesterol level
* **fasting_blood_sugar** — Fasting blood sugar status
* **rest_ecg** — Resting ECG result
* **Max_heart_rate** — Maximum heart rate achieved
* **exercise_induced_angina** — Exercise-induced chest pain
* **oldpeak** — ST depression induced by exercise
* **slope** — Slope of peak exercise ST segment
* **vessels_colored_by_flourosopy** — Number of major vessels colored by fluoroscopy
* **thalassemia** — Blood disorder condition
* **target** — Prediction label

---

## Project Objectives

* Clean dataset
* Handle missing values
* Perform Exploratory Data Analysis (EDA)
* Train classification model
* Evaluate using multiple metrics
* Identify important predictive features

---

## Technologies Used

* Python
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

---

## Data Preprocessing

The following preprocessing steps were performed:

1. Loaded dataset into Pandas DataFrame
2. Checked for missing values
3. Removed duplicates
4. Encoded categorical features into numeric form
5. Split data into features and target
6. Scaled features using StandardScaler

This ensured clean and model-ready data.

---

## Exploratory Data Analysis (EDA)

EDA was performed to understand patterns and relationships.

### Visualizations Used

* Count plot
* Histograms
* Correlation heatmap
* Box plots

### Key Observations

* Chest pain type strongly affects prediction
* Maximum heart rate is an important indicator
* Exercise-induced angina contributes significantly
* Some features contain outliers

---

## Machine Learning Model

Model used:

### Logistic Regression

Logistic Regression is a supervised learning algorithm used for binary classification.

It predicts probability using the sigmoid function:

P(y=1) = 1 / (1 + e^(-z))

Advantages:

* Simple and efficient
* Good for binary classification
* Easy to interpret

---

## Train-Test Split

Dataset split:

* 80% Training Data
* 20% Testing Data

Training data was used to fit the model.
Testing data was used to evaluate performance.

---

## Evaluation Metrics

### Accuracy

Accuracy measures the percentage of correct predictions.

Accuracy = Correct Predictions / Total Predictions

### Model Accuracy

**Accuracy = 80.33%**

This means the model correctly classified approximately 80% of patient records.

---

### Confusion Matrix

Confusion Matrix Results:

* True Negative (TN) = 25
* False Positive (FP) = 7
* False Negative (FN) = 5
* True Positive (TP) = 24

Interpretation:

* 25 healthy patients were correctly classified
* 24 patients with heart disease were correctly identified
* 7 healthy patients were wrongly predicted as diseased
* 5 diseased patients were missed

False negatives are especially important in healthcare because missing a diseased patient can be dangerous.

---

## ROC Curve

ROC Curve was used to evaluate classification performance across thresholds.

It compares:

* True Positive Rate
* False Positive Rate

A curve closer to the top-left indicates better performance.

---

## Feature Importance

Important features affecting prediction include:

* Chest Pain Type
* Max Heart Rate
* Exercise-Induced Angina
* Oldpeak
* Number of Vessels
* Thalassemia

These features had the strongest impact on prediction.

---

## Skills Demonstrated

* Binary Classification
* Medical Data Analysis
* Exploratory Data Analysis
* Logistic Regression
* Model Evaluation
* Confusion Matrix Interpretation
* ROC-AUC Analysis
* Feature Importance Analysis

---

## Project Workflow

1. Import libraries
2. Load dataset
3. Clean data
4. Perform EDA
5. Encode categorical data
6. Train model
7. Evaluate performance
8. Interpret results

---

## Future Improvements

Possible enhancements:

* Try Decision Tree or Random Forest
* Hyperparameter tuning
* Use XGBoost
* Deploy as healthcare web application
* Build real-time prediction dashboard

---

## Conclusion

This project demonstrates how Machine Learning can assist in healthcare prediction. Using patient medical data, the model predicts whether a person is at risk of heart disease.

The Logistic Regression model achieved **80.33% accuracy**, showing good predictive capability. Such systems can support early diagnosis and help healthcare professionals make better clinical decisions.
