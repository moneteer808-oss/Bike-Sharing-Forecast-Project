# Forecast Daily Bike Rental Demand Using Time Series Models

## Project Overview
Analysis of daily bike rental demand in Washington, DC (2011-2012) using time series modeling techniques to understand patterns and forecast future demand.

## Data Source
- **Dataset**: Bike Sharing Dataset from UCI Machine Learning Repository
- **Period**: 2011-2012
- **Records**: Daily bike rental transactions with weather and seasonal information
- **Source**: [UCI Bike Sharing Dataset](https://archive.ics.uci.edu/ml/datasets/bike+sharing+dataset)

## Key Findings

### Data Exploration
- Strong positive correlation between temperature and rentals (`cor = 0.627`)
- Seasonal patterns: Peak demand in Summer (mean = 5,644/day), lowest in Winter (mean = 2,604/day)

### Time Series Analysis
- Clear seasonal patterns and upward trend observed
- SMA(10) smoothing effectively revealed underlying trends
- Original series was non-stationary; became stationary after first-order differencing

### Forecasting Model
- ARIMA(1,0,1) model fitted to differenced series
- 25-day forecast shows stable changes around zero in daily rental variations

### Packages Used
- timetk, dplyr, ggplot2, lubridate, forecast, TTR, tseries

### Analysis Steps
- Data loading and exploration
- Time series visualization and smoothing
- Stationarity assessment and decomposition
- ARIMA model fitting and forecasting
  
### Conclusion
- The analysis demonstrates effective application of time series methods to real-world rental data, revealing strong weather dependencies and seasonal patterns. The modeling approach provides a foundation for business demand forecasting.
---

Moneteer808@gmail.com 2025
