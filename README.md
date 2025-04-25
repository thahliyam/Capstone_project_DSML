Capstone Project: Predicting Online Shopper Purchasing Intentions
Project Overview
This project utilizes the Online Shoppers Purchasing Intention Dataset from the UCI Machine Learning Repository to predict whether a visitor to an e-commerce platform will make a purchase. The dataset consists of 12,330 records and 18 features, including numeric and categorical variables that describe user behavior during each session.

Target Variable
Revenue: A binary indicator of whether the session resulted in a purchase (1 = purchase, 0 = no purchase).

Features
The dataset includes various features describing user behavior during a session:

Administrative: Number of pages visited in the "Administrative" section.

Informational: Number of pages visited in the "Informational" section.

ProductRelated: Number of pages visited in the "ProductRelated" section.

ProductRelated_Duration: Duration spent on "ProductRelated" pages.

BounceRates: Percentage of sessions where the visitor left the website after viewing a single page.

ExitRates: Percentage of sessions where the visitor exited the website after viewing the page.

VisitorType: Type of visitor (New Visitor, Returning Visitor).

TrafficType: Source of traffic (Direct, Referral, etc.).

Month: Month in which the session took place.

Weekend: Boolean indicating whether the session occurred on the weekend.

Objective
The goal of this project is to analyze the dataset and predict the likelihood of a visitor making a purchase based on various user behavior features. We will explore the dataset, perform necessary preprocessing, and build multiple classification models to find the best-performing one for predicting Revenue.

Steps in the Project
1. Data Loading and Exploration
The dataset was loaded and explored to understand its structure, identify missing values, and detect potential issues.

Columns like Revenue and Weekend were originally not in numeric format and were converted for better analysis.

2. Data Cleaning and Preprocessing
Handling Missing Values: Missing values were identified and appropriately imputed.

Outlier Detection and Treatment: Outliers were handled using quantile-based capping methods.

Two capping strategies were tested:

0.01 to 0.99 quantile range.

0.05 to 0.95 quantile range.

Feature Encoding: Categorical variables were one-hot encoded, and numerical features were scaled.

Skewness Transformation: After outlier treatment, the skewness of the distribution was recalculated, with the 0.05 to 0.95 capping range showing better balance.

3. Feature Engineering and Preprocessing Pipeline
The preprocessing steps (scaling and encoding) were incorporated into a pipeline using ColumnTransformer and Pipeline from scikit-learn. This ensures a reproducible workflow.

4. Model Building and Evaluation
Multiple classification models were tested to predict Revenue:

Logistic Regression

Decision Tree

Random Forest

Hyperparameter Tuning: RandomizedSearchCV was used to tune model hyperparameters, optimizing the performance of each model.

5. Model Performance Metrics
The performance of each model was assessed using the following metrics:

Accuracy

Precision

Recall

F1-Score

ROC-AUC

The best-performing model was selected based on these metrics, offering reliable predictions for user purchase intentions.

Author
This project was completed by Thahliya M as part of the Data Science and Machine Learning Capstone Project.

