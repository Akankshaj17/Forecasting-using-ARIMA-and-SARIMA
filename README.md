# Forecasting-Using-ARIMA-and-SARIMA

# 🔍 Introduction

- Time series forecasting is a crucial tool in predictive analytics, especially when analyzing trends over time, such as sales, demand, or usage patterns. This project explores two classical statistical methods for time series forecasting:

ARIMA (AutoRegressive Integrated Moving Average)

SARIMA (Seasonal ARIMA)

- These models are particularly useful when working with univariate time series data that exhibits autocorrelation, trends, or seasonality. We apply both methods to a real-world dataset of monthly champagne sales to model and forecast future values.

# 🧠 Key Concepts:
ARIMA: Combines autoregression (AR), differencing (I), and moving average (MA) to model time series data.

SARIMA: Extends ARIMA by incorporating seasonal components (i.e., repeated patterns at fixed intervals).

# 🧪 Steps Performed

## 1. Data Loading & Cleaning
- Loaded perrin-freres-monthly-champagne.csv dataset using pandas.

- Checked for missing values and dropped irrelevant or NaN rows.

- Converted the 'Month' column to datetime and set it as the index.

## 2. Initial Visualization

- Plotted the sales data over time.

- Observed clear seasonality and upward trends, indicating the need for advanced modeling.

## 3. Stationarity Check

- Used the ADF (Augmented Dickey-Fuller) test to check if the series is stationary.

- Applied differencing and seasonal differencing to make the series stationary.

## 4. ACF & PACF Plots

Generated AutoCorrelation Function (ACF) and Partial AutoCorrelation Function (PACF) plots to determine AR and MA terms for model selection.

## 5. Model Building – ARIMA

- Fit an ARIMA(1,1,1) model on the differenced data.

- Plotted predictions against actuals.

- Observed that ARIMA was not capturing seasonality well.

## 6. Model Building – SARIMA

- Fit a SARIMA(1,1,1)(1,1,1,12) model.

- Generated forecasts and visualized them.

- This model handled seasonal variations much more accurately.

# 📌 Observations & Conclusion

- As we can see, the ARIMA model was unable to model the seasonal patterns, which led to poor forecasting accuracy.

- The SARIMA model, however, significantly improved the forecast, capturing seasonal dips and spikes effectively.

- Thus, SARIMA is better suited for this type of seasonal time series data.

# 💻 Technologies Used

- Python

- Jupyter Notebook

- pandas, matplotlib, statsmodels
