# Pairs Trading Algorithm using Mean Reversion
An Implementation of a Pairs Trading Trading Strategy based on Mean Reversion

## Background
Pairs trading strategies involves identify some statistically related pair of assets and simulatenously matching a long position with a short position on the two. Its foundations lie in the financial theory of mean reversion which believes that assets will eventually deviate towards its long term average. 

Financial variables are typically known to be non-stationary, which means that the time series data has properties that change over time. So, we want to find pairs that are cointegrated. Cointegration refers to when we have two time series data that are respectively non-stationary, but some linear combination of the two is.

To look for cointegrated pairs, we will utilize the **Engle-Granger Two-Step Cointegration test**. This is broken down into by creating residuals by regressing one variable on the other and then applying the **Augmented Dickey-Fuller test** to test for stationarity on the residual.

Due to running many cointegration tests, we are liable to the multiple comparison bias which refers to when we get falsely many statistically significant p-values because of the sheer large number of tests we run. To counteract this, I utilized the **Benjamini-Hochberg (BH) Procedure** which is commonly used to reduce Type I Errors.

