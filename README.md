# Bike Sharing Forecast Project

**Author:** Moneteer  
**Created:** 2025

This project analyzes daily bike rental demand in Washington, DC (2011-2012) using time series models in R. The goal is to explore the data, uncover patterns, and forecast short-term bike rental demand.

---

## Project Structure
-  bike-sharing-forecast/
-  ├── data/                       # Raw and processed datasets
-  ├── reports/                    # Analysis reports (.Rmd, HTML)
-  ├── guided_tasks.pdf            # Step-by-step guide for the project
-  ├── bike-sharing-forecast.Rproj # RStudio project file

---
---

## 📖 Data Description

- **Source:** [UCI Bike Sharing Dataset](https://archive.ics.uci.edu/ml/datasets/bike+sharing+dataset) (part of Coursera Project Network)
- **Time Period:** 2011–2012  
- **Content:** Daily count of bike rentals (`cnt`) with weather and seasonal features.  
- **Relevant Paper:** Fanaee-T, Hadi, and Gama, Joao. *Event labeling combining ensemble detectors and background knowledge*, Progress in Artificial Intelligence (2013), Springer Berlin Heidelberg.

---

## Methodology

1. **Data Loading & Exploration**
   - Inspect dataset, summary statistics, and correlations.
   - Analyze rentals by season and temperature.

2. **Time Series Visualization**
   - Interactive line plots by year.
   - Smoothing with SMA(10) to identify trends.

3. **Time Series Cleaning & Smoothing**
   - Use `forecast::tsclean()` to handle outliers and missing values.
   - Apply moving average smoothing for trend visualization.

4. **Decomposition & Stationarity**
   - Decompose series using STL.
   - Check stationarity with Augmented Dickey-Fuller (ADF) test.
   - Apply first-order differencing to achieve stationarity.

5. **ARIMA Forecasting**
   - Fit ARIMA model on differenced series.
   - Forecast the next 25 days to predict changes in daily rentals.

---

## Key Findings

- Strong positive correlation between temperature and rentals (`cor(temp, cnt) = 0.627`).  
- Peak rentals occur in **Summer** (≈5,644/day), lowest in **Winter** (≈2,604/day).  
- Series is non-stationary initially; first-order differencing achieves stationarity.  
- ARIMA forecasting predicts **stable changes** in daily rentals over the next 25 days.  

---

## How to Reproduce

1. Open `bike-sharing-forecast.Rproj` in RStudio.  
2. Install required packages:

install.packages(c("timetk", "dplyr", "forecast", "tseries", "ggplot2", "lubridate", "TTR"))

3. Knit the reports/Forecast-daily-bike-rental-demand-using-time-series-models.Rmd to produce HTML, PDF, or Word outputs.

## Notes
- Forecast are for changes in daily rentals, not absolute counts.
- Future improvements can include holidays, events, promotions as external regressors.
