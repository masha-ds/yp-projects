# Taxi Orders Forecasting
----
## Description

The company has collected historical data on taxi orders at airports. To attract more drivers during peak hours, we need to forecast the number of taxi orders for the next hour. We will build a model for this prediction.
The RMSE metric on the test set should not exceed 48.

## Tools and skills

_decompose, LGBMRegressor, CatBoostRegressor, LinearRegression, ElasticNet, FunctionTransformer_

## Steps

1. Data loaded and initial inspection conducted.
2. Data preprocessing performed.
3. Data prepared for model training.
4. Several machine learning models trained
5. Best model selected and its performance evaluated on the test set.

## Results

To prepare the data for model training, we performed resampling at one-hour intervals and created new features: time-based features (hour and day of the week) as well as 24 lag features corresponding to the previous 24 hours, allowing the model to consider previous hours when making predictions. We also set the moving average window size to 24 hours.

After comparing the results of different models, we determined that the CatBoostRegressor with a learning rate of 0.05, a maximum tree depth of 6, and 600 trees in the ensemble showed the best performance in terms of RMSE on the training data. The LGBMRegressor was the second-best in terms of prediction quality, with a slightly lower performance but significantly faster training time.

The RMSE metric on the test set for the CatBoostRegressor model was 41.02, which is significantly better than forecasting using the previous values in the series (58.88).

The most important features for the prediction were the time shifts by one and twenty-four hours, and the hour of the day, which is logical given the cyclical nature of taxi orders throughout the day.