# Taxi order forecasting

Predicting the number of taxi orders for the next hour at airports. Aimed at optimizing driver availability during peak times.

**What's done:**

- Data was loaded, explored, and resampled to one hour intervals.
- Data analysis was conducted: the provided time series is non-stationary with an upward trend and seasonality.
- Data was prepared for training: columns with month, day, day of the week, hour, moving averages, and lags were added.
- Several models were trained:
    - Linear Regression
    - CatBoost
    - Random Forest
    
- The best result was achieved by the Random Forest model: RMSE = 25.566685.
- The result on the test data: RMSE = 43.6634.

While the metrics meet the task requirements, they noticeably decrease compared to the training set. SARIMA is expected to provide a better result.
