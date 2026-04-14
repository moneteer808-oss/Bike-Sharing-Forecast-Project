# Bike Demand Forecasting for Operational Planning

**Author:** Moneteer  
**Created:** 2025

This project analyzes daily bike rental demand in Washington, DC (2011–2012) using time series models in R. The objective is to generate actionable demand forecasts that support operational planning and resource allocation.

This project demonstrates how data-driven forecasting can be translated into practical operational decisions.


---

## Project Structure
-  bike-sharing-forecast/
-  ├── data/                       # Raw and processed datasets
-  ├── reports/                    # Analysis reports (.Rmd, HTML)
-  ├── guided_tasks.pdf            # Step-by-step guide for the project
-  ├── bike-sharing-forecast.Rproj # RStudio project file

---

## 📖 Data Description

- **Source:** [UCI Bike Sharing Dataset](https://archive.ics.uci.edu/ml/datasets/bike+sharing+dataset) (part of Coursera Project Network)
- **Time Period:** 2011–2012  
- **Content:** Daily count of bike rentals (`cnt`) with weather and seasonal features.  
- **Relevant Paper:** Fanaee-T, Hadi, and Gama, Joao. *Event labeling combining ensemble detectors and background knowledge*, Progress in Artificial Intelligence (2013), Springer Berlin Heidelberg.

---

## Technical Approach

- Time series analysis and decomposition (STL)
- Stationarity testing and differencing
- ARIMA modeling for forecasting
- Data cleaning and smoothing techniques

---

## Key Findings

- Demand is strongly influenced by temperature, with higher rentals occurring during warmer conditions (correlation = 0.627)
- Clear seasonal patterns are observed:
   - Peak rentals occur in **Summer** (≈5,644/day), lowest in **Winter** (≈2,604/day).  
- Demand patterns are consistent and predictable over time, enabling reliable short-term planning
- Forecast results indicate relatively stable demand trends over the next 25 days, enabling short-term operational planning


---

## So What?

Without demand forecasting and proactive allocation:

- Bike shortages are likely during peak periods, reducing service availability
- Excess bikes remain unused during low-demand periods, lowering operational efficiency

These demand patterns indicate that allocation decisions can be optimized using forecast-driven planning.

---

## Operational Recommendation

Based on forecasted demand patterns:

- Prioritize bike allocation during peak demand periods (e.g., commuting hours in summer), where demand significantly exceeds baseline levels
- Reallocate bikes from low-demand periods (e.g., winter) to high-demand periods to improve utilization
- Pre-position bikes in high-demand locations ahead of peak periods to reduce shortages
- Improve resource utilization and reduce service inefficiencies during demand fluctuations


## Implementation Use Case

This model can support:
- Daily operational planning
- Resource allocation decisions
- Demand monitoring and performance tracking

## Limitations & Next Steps

- Forecasts are based on historical patterns and may be less accurate during unusual events (e.g., extreme weather)
- Current model does not include external factors such as holidays or special events

Future improvements:
- Incorporate external regressors (holidays, events, promotions)
- Develop a real-time dashboard for monitoring demand and allocation

## How to Reproduce

1. Open `bike-sharing-forecast.Rproj` in RStudio.  
2. Install required packages:

```r
install.packages(c("timetk", "dplyr", "forecast", "tseries", "ggplot2", "lubridate", "TTR"))
```
3. Knit the reports/Forecast-daily-bike-rental-demand-using-time-series-models.Rmd to produce HTML, PDF, or Word outputs.

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

## Notes
- Forecasts are for changes in daily rentals, not absolute counts.
- Future improvements can include holidays, events, promotions as external regressors.
