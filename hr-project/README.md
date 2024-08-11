# Predicting Employee Satisfaction and Attrition
----
## Description

The goal of the project is to predict employee job satisfaction levels and instances of turnover based on the available data.

## Tools and skills

_pipeline, ColumnTransformer, Encoders, Scalers, GridSearchCV, RandomizedSearchCV, LinearRegression, LogisticRegression, KNeighborsClassifier, DecisionTreeClassifier, DecisionTreeRegressor, SVC_

## Steps

1. Data Preprocessing: Obtaining employee data, including their characteristics and satisfaction levels, as well as cleaning and preparing this data for analysis.

2. Exploratory Data Analysis: Analyzing the main characteristics of employees and their relationship with job satisfaction levels. Identifying significant features for model building.

3. Developing and training a machine learning model based on the selected features to predict employee satisfaction levels.

4. Model Evaluation: Assessing the quality and effectiveness of the built model on test data using appropriate evaluation metrics.

## Results

The best model for predicting satisfaction levels was the DecisionTreeRegressor with the following hyperparameters: max_depth=19, min_samples_leaf=2, min_samples_split=6. The model performed well on both training and test data, and no overfitting was observed. The most influential factors in the predictions were supervisor evaluation, work experience, and the absence of contract violations.

For predicting employee attrition, we trained three models—DecisionTreeClassifier, KNeighborsClassifier, and LogisticRegression—and selected the best model based on the ROC-AUC metric from cross-validation results. We considered two versions of the input data: a full feature set, including predicted employee satisfaction levels, and a set without features that had weak correlations with the target—such as the 'dept' feature—and without features that were highly correlated with others, specifically 'supervisor_evaluation'.

In all cases, the best model was KNeighborsClassifier. On data without redundant features, with the number of neighbors set to 14 and the Manhattan distance metric, it achieved an ROC AUC of 0.92. This is a relatively high value, indicating that the model confidently separates the classes and is capable of making accurate predictions in the context of employee attrition forecasting. The features that most strongly influenced the model’s classification were work experience, employee satisfaction, job position, workload, and salary level.