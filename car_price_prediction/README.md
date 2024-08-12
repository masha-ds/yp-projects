# Car Price Prediction
----
## Description

A used car sales service is developing an application to attract new customers. It allows users to quickly find out the market value of their car. We have historical data including technical specifications, trims, and car prices. We need to build a model to determine car prices.

To develop a model that accurately determines car prices based on the provided data. The client has set three key requirements for the project:

- High prediction accuracy.
- Fast prediction speed.
- Minimal training time.
To achieve these goals, research will be conducted using various machine learning models, including complex methods such as gradient boosting and simpler algorithms. This will help choose the most effective model in terms of accuracy, speed, and training time.

## Tools and skills

_ColumnTransformer, sklearn, LGBMRegressor, CatBoostRegressor, SHAP_

## Steps

1. Data Loading and Preparation:

- Clean the data from missing values, duplicates, and anomalies.
- Prepare features for model training.

2. Model Training:

- Tune hyperparameters for models.
- Train models.

3. Model Performance Analysis:

- Compare models based on RMSE (Root Mean Squared Error).
- Evaluate prediction speed.
- Evaluate training time.

## Results

We encountered a significant amount of missing values in the data, which presented a challenge for analysis. Overall, the dataset was quite raw and required substantial preprocessing before it could be effectively used for modeling.

LGBMRegressor has the best RMSE value, indicating the lowest mean squared error and the highest prediction accuracy compared to other models. However, LGBMRegressor takes a comparably long time to make predictions. The RMSE value for CatBoostRegressor is slightly worse than that of LGBMRegressor.
Considering all the results, the most optimal model for predicting car prices is LGBMRegressor with 1000 trees in the ensemble and an L2 regularization coefficient of 0.1.