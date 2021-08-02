# JPY_vs_USD

## Background

The financial departments of large companies often deal with foreign currency transactions while doing international business. As a result, they are always looking for anything that can help them better understand the future direction and risk of various currencies. Hedge funds, too, are keenly interested in anything that will give them a consistent edge in predicting currency movements.

In this analysis, time-series tools would be used in order to predict future movements in the value of the Japanese yen versus the U.S. dollar.



### 1) [Time Series Forecasting](Code/time_series_analysis.ipynb)

```

Conclusions
Questions:
Based on your time series analysis, would you buy the yen now?
Is the risk of the yen expected to increase or decrease?
Based on the model evaluation, would you feel confident in using these models for trading?

Findings via analysis:
GARCH Model has the lowest P Value, and hence it a good fit for timeseries forecasting of the dataframe. Given that GARCH model predicts that Variance is going to increase for Yen vs Dollar, hence Risk of Forex conversion is more in future for a portfolio that holds Yen. Hence, it would be advisable not to buy Yen now. I would feel confident is utilizing these models for trading based on best fit approach.

```


### 2) [Linear Regression Modeling](Code/regression_analysis.ipynb)

```

Conclusions
Findings via analysis:
The Test data has a lower RMSE than the training data, i.e., the model performs better on the test data. This may have been caused due to the very small test data size (return window) compared to the training data size. The training data has generalized the prediction very well.

In the test data, the Actual return has a high Variance, and a low bias against the predicted returns.

So, given the RMSE comparisons, and Variance vs bias observations, it can be predicted that this Linear Regression Model predicts the trend very closely, but misses on predicting the magnitude of returns because the training set is generalized over a much longer time window.

To predict the returns more closely, the training data size could be comparable to the test data size and could be from the time window which has Market properties closer to the test data window.


```
