# Stock Price & Exchange Rate Analysis and Forecasting

A collection of time-series forecasting projects applying deep learning and statistical models to financial data, covering both equity markets and foreign exchange rates.

---

## Project Overview

| Notebook | Target | Model | Task |
|---|---|---|---|
| [AAPL Stock Price Analysis & Prediction](https://github.com/laingangiang2006/Stock-Price-And-Exchange-Rate-Analysis/tree/main/Stock%20Price%20Analysis%20%26%20Prediction) | Apple Inc. (AAPL) | LSTM (Deep Learning) | Stock price prediction |
| [AUD-USD Exchange Rate Analysis & Prediction](https://github.com/laingangiang2006/Stock-Price-And-Exchange-Rate-Analysis/tree/main/AUD-USD%20Exchange%20Rate%20Analysis%20%26%20Prediction) | AUD/USD Exchange Rate | SARIMA (Statistical) | Exchange rate forecasting |

---

## Projects

### 1. AAPL Stock Price Prediction — LSTM

**Directory:** [Stock Price Analysis & Prediction](https://github.com/laingangiang2006/Stock-Price-And-Exchange-Rate-Analysis/tree/main/Stock%20Price%20Analysis%20%26%20Prediction)

Predicts Apple's stock closing price using a Long Short-Term Memory (LSTM) neural network, which is a type of recurrent neural network well-suited for sequential and time-series data.

**Key steps:**
- Data collection via yfinance (or similar)
- Exploratory data analysis (EDA) and visualization
- Data preprocessing & normalization (MinMaxScaler)
- Sequence generation for LSTM input windows
- Model architecture: stacked LSTM layers + Dense output
- Training, evaluation, and prediction
- Metrics: RMSE, MAE

---

### 2. AUD/USD Exchange Rate Analysis — SARIMA

**Directory:** [AUD-USD Exchange Rate Analysis & Prediction](https://github.com/laingangiang2006/Stock-Price-And-Exchange-Rate-Analysis/tree/main/AUD-USD%20Exchange%20Rate%20Analysis%20%26%20Prediction)

Analyzes and forecasts the Australian Dollar to US Dollar exchange rate using SARIMA (Seasonal AutoRegressive Integrated Moving Average), which is a classical statistical approach for time-series with seasonality.

**Key steps:**
- Data loading and preprocessing
- Stationarity testing (ADF test)
- ACF/PACF analysis for parameter selection
- SARIMA model fitting and diagnostics
- Forecasting future exchange rate values
- Metrics: AIC, BIC, RMSE

---

## Technologies Used

| Library | Purpose | Used In |
|---|---|---|
| Pandas, NumPy | Data manipulation | Both notebooks |
| Matplotlib, Seaborn | Visualization | Both notebooks |
| Scikit-learn | Preprocessing & evaluation metrics | Both notebooks |
| Tensorflow / keras | LSTM model | AAPL notebook |
| Statsmodels | SARIMA model | AUD/USD notebook |
| yfinance | Financial data retrieval | Both notebooks |

---

## Results Summary

| Project | Model | Notes |
|---|---|---|
| AAPL Stock Prediction | LSTM | Deep learning model capturing non-linear price patterns |
| AUD/USD Forecasting | SARIMA | Statistical model with seasonality and trend decomposition |

---

## Notes

- Stock and exchange rate data is fetched dynamically; results may differ depending on the date of execution.
- These projects are for **educational purposes** and should not be used for actual trading or investment decisions.

---

## Author

**laingangiang2006** - [GitHub Profile](https://github.com/laingangiang2006)

---

## License

This portfolio is for educational use.
