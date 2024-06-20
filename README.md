# Monthly Beer Production Forecasting with ARIMA and SARIMA Models
## Overview
Welcome to the Monthly Beer Production Forecasting Project README. This document provides an in-depth exploration of time series forecasting using ARIMA (AutoRegressive Integrated Moving Average) and SARIMA (Seasonal ARIMA) models. The project focuses on predicting monthly beer production based on historical data, leveraging advanced time series analysis techniques.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Stationarity Testing](#stationarity-testing)
- [ARIMA Model](#arima-model)
- [SARIMA Model](#sarima-model)
- [Forecasting](#forecasting)
- [Evaluation Metrics](#evaluation-metrics)
- [Conclusion](#conclusion)


## Introduction
Forecasting beer production is crucial for breweries to manage inventory, plan resources, and meet consumer demand efficiently. This project applies ARIMA and SARIMA models to historical monthly beer production data to generate accurate forecasts. These models help capture both the trend and seasonal patterns inherent in the data.

## Dataset
The dataset used in this project contains monthly beer production figures from January 1956 to December 1975. It includes 240 entries, with each entry representing the monthly beer production in Australia.

## Key attributes of the dataset:

- Monthly beer production: The quantity of beer produced each month.
- Date range: January 1956 to December 1975.

## Exploratory Data Analysis
Exploratory Data Analysis (EDA) was conducted to understand the underlying patterns in the data. Key findings include:

- Trend Analysis: The data shows an upward trend in beer production over the years.

- Seasonality: There is a clear seasonal pattern, with production peaking during certain months each year.
Visualizations such as bar plots and pivot tables were used to display the monthly and yearly production trends, highlighting both the annual increase and the seasonal variations.

## Stationarity Testing
Stationarity is a key assumption in time series modeling. The Augmented Dickey-Fuller (ADF) test was used to check for stationarity:

The initial test indicated that the series is non-stationary.
After differencing the series once, the ADF test confirmed stationarity, with a p-value less than the significance level of 0.05.

## ARIMA Model
The ARIMA model was applied to the stationary data. The model parameters (p, d, q) were determined based on the autocorrelation and partial autocorrelation plots:

**Order of ARIMA**: (1, 1, 1)
The model summary indicated significant coefficients for the AR and MA terms, with good overall model fit.
However, the initial forecasts from the ARIMA model did not account for the seasonality in the data, indicating the need for a more advanced model.

## SARIMA Model
To incorporate seasonality, the SARIMA model was used. The parameters for the seasonal component were added to the ARIMA model:

**Order of SARIMA**: (1, 1, 1) x (1, 1, 1, 12)
The model showed a significant improvement in the fit, capturing both the trend and seasonal patterns.
The SARIMA model provided better forecast accuracy by accounting for the seasonal variations in beer production.

## Forecasting
The SARIMA model was used to forecast monthly beer production for the next three years beyond the available data. The forecasts aligned well with the historical trend and seasonal patterns observed in the data.

## Evaluation Metrics
The model performance was evaluated using standard metrics such as:

- Mean Squared Error (MSE): To measure the average of the squares of the errors.
  
- Root Mean Squared Error (RMSE): To measure the square root of the average of the squared differences between the forecasted and actual values.
  
The SARIMA model outperformed the ARIMA model in terms of lower MSE and RMSE, confirming its superior ability to handle seasonality in the data.

## Conclusion
The Monthly Beer Production Forecasting Project demonstrates the application of ARIMA and SARIMA models to time series data. By incorporating both trend and seasonality, the SARIMA model provided more accurate and reliable forecasts. These forecasts can help breweries in making informed decisions related to production planning and resource management.

For further details on the implementation and results, please refer to the project documentation and visualizations included in this repository.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

