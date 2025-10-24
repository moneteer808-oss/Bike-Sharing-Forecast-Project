# Bike Sharing Forecast Project

A time series forecasting analysis of daily bike rental demand in Washington, DC (2011–2012) using R.

## 📊 Key Insights
- Strong correlation between temperature and rentals (`cor = 0.63`)
- Summer rentals (~5,644/day) are more than double winter (~2,604/day)
- ARIMA(1,0,1) model applied to stationary differenced series
- Forecast shows stable short-term demand changes

## 📁 Files
- [`index.html`](index.html) 
-  **Live report** (viewable in browser)  
- [`Forecast-daily-bike-rental-demand-using-time-series-models.Rmd`](Forecast-daily-bike-rental-demand-using-time-series-models.Rmd) – Source code

## 📚 Data Source
Built-in dataset from the `timetk` R package (originally from [UCI Bike Sharing Dataset](https://archive.ics.uci.edu/ml/datasets/bike+sharing+dataset))
