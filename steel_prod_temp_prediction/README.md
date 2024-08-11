# Optimizing Steel Production: Temperature Prediction and Process Stability Enhancement
----
## Description

To optimize production costs, the steel plant has decided to reduce energy consumption during the steel processing stage. To achieve this, the plant needs to control the alloy temperature. Our task is to build a model that will predict this temperature, with a maximum MAE threshold of 6.8 set for evaluating the model's performance on test data.

## Tools and skills

_pipeline, GridSearchCV, PolynomialFeatures, LinearRegression, Lasso, Ridge, ElasticNet, CatBoostRegressor, LGBMRegressor, RandomForestRegressor, SHAP_

## Steps

1. Data loaded and initial inspection conducted.
2. Exploratory data analysis and data preprocessing performed.
3. Data from different sources merged into a single dataframe.
4. Data prepared for model training.
5. Several machine learning models trained.
6. Best model selected and its performance evaluated on the test set.
7. General conclusion made and recommendations provided to the client.

## Results

To optimize the production process and reduce energy consumption, the best model for predicting alloy temperature was selected. The CatBoostRegressor model showed good results on the test data: MAE of 5.87 (the model's predictions deviate from the actual values by 5.87 °C), meeting the required accuracy level. The key features that had the most significant impact on the predictions include the initial temperature, the number of heating operations, the average heating time, as well as the volume and quantity of bulk and wire materials used.