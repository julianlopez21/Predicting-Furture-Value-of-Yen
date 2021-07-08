# Predicting Future Value of Yen

In this project I loaded historical USD-JPY exchange rate futures data and applied time series analysis and modeling to determine whether there is any predictable behavior. Then, I built a linear regression model to predict Yen futures returns.

## Time Series Forecasting

After cleaning the data, I used statsmodels' Hodrick-Prescott Filter to decompose the historical settlement price data into trend and noise. Then I created and compared the following models to forecast the settlement price:
- ARMA Model with an order of (2, 1)
- ARIMA model with an order of (5, 1, 1)

Then, I created a GARCH model to forecast the volatility of the Yen futures returns.

## Linear Regression Modeling

After calculating returns and adding a lagged returns column, I split the data into training and testing sets. Then, I created a linear regression model and made predictions using the testing data. I compared the performance of the model using out-of-sample data and in-sample data. Comparing the root-mean-squared error I concluded the model performed better using the out of sample data, which suggests I likely need better training data than just 1 lag of returns.
