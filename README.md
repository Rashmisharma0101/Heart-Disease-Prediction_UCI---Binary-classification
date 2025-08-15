# Purpose
This project applies data science and machine learning to predict the likelihood of heart disease from patient health indicators.
It’s designed to showcase skills in data preprocessing, exploratory analysis, model selection, and evaluation.

# Project Overview
This project predicts the likelihood of heart disease using the UCI Heart Disease dataset.
It applies data preprocessing, exploratory data analysis (EDA), and machine learning models to classify patients as having or not having heart disease.

# Dataset
* Source: UCI Machine Learning Repository
* Instances: 303
* Features: 14 (age, sex, chest pain type, blood pressure, cholesterol, etc.)
* Target - 'num': 0 = No Heart Disease, 1 = Heart Disease
 Initially there were multiple classes as 0,1,2,3,4
  0 - no Heart disease
  1,2,3,4 - indicating level of heart disease where 4 is  the most dangerous
  As there is very limited data (<1000 rows), amost all classes overlap with each other and after model tuning and selection

  * Classification Report from first approach:
              precision    recall  f1-score   support

           0       0.82      0.80      0.81        82
           1       0.60      0.47      0.53        53
           2       0.37      0.45      0.41        22
           3       0.25      0.33      0.29        21
           4       0.29      0.33      0.31         6

    accuracy                           0.60       184
   macro avg       0.47      0.48      0.47       184
weighted avg       0.62      0.60      0.61       184


  In this notebook, I have converted classes 1,2,3,4 to class 1 only and predicted 0 and 1 on test set
  * Classification Report from Second approach:
  precision    recall  f1-score   support

           0       0.83      0.78      0.81       123
           1       0.83      0.88      0.85       153

    accuracy                           0.83       276
   macro avg       0.83      0.83      0.83       276
weighted avg       0.83      0.83      0.83       276

Second approach gave much better recall and accuracy for both the classes 0 and 1
For first approach, please visit - https://www.kaggle.com/code/rashmisharma123/heart-disease-prediction-all-classes

* Steps Performed
- Data Cleaning
- Handled missing values
- Converted categorical features to numerical form
- Exploratory Data Analysis (EDA)
- Distribution of features
- Class imbalance check
- One-hot encoding for categorical features

* Model Building
- XGBoost Classifier (Hyperparameter Tuning)
  
* Model Evaluation
- Accuracy, Precision, Recall, F1-score














