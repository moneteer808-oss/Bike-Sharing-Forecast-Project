# Bike Sharing Demand Forecast (Time Series Analysis in R)

A complete time series forecasting project analyzing daily bike rental demand in Washington, DC (2011–2012) using R.

## Key Findings
- **Strong correlation** between temperature and rentals (`cor = 0.63`)
- **Summer demand** (~5,644 rentals/day) is more than double **winter** (~2,604/day)
- Time series was **non-stationary** → made stationary via **first-order differencing**
- Best-fitting model: **ARIMA(1,0,1)** on differenced data
- Short-term forecast shows **stable daily changes** (no strong trend)

## Files
- [`index.html`](index.html) – **Live interactive report** (viewable in browser)
- [`Forecast-daily-bike-rental-demand-using-time-series-models.Rmd`](Forecast-daily-bike-rental-demand-using-time-series-models.Rmd) – Full R Markdown source code

## Data Source
Built-in dataset from the **`timetk`** R package, originally from:  
[UCI Bike Sharing Dataset](https://archive.ics.uci.edu/ml/datasets/bike+sharing+dataset)

## View the Full Report
👉 [Open Live Report](https://moneteer808-oss.github.io/Bike-Sharing-Forecast-Project/)
