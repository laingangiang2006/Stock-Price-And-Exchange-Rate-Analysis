# AUD-USD Exchange Rate Analysis & Prediction

A time series data science project analyzing and forecasting the AUD/USD exchange rate using historical OHLCV data (2020–2026) with SARIMA modeling.

---

## Overview

This notebook analyzes the historical AUD/USD exchange rate and builds a SARIMA (Seasonal AutoRegressive Integrated Moving Average) forecasting model to predict future exchange rates for the next **60 trading periods**. The analysis covers data from January 2020 to June 2026 (1,688 trading days).

I also exported the dataset from this project to Kaggle, available here: [AUD-USD Exchange Rate Analysis and Forecasting](https://www.kaggle.com/datasets/laingangiang2006/aud-usd-exchange-rate-analysis-and-forecasting).

If you don't want to run and check my code locally, you can check it through my [Kaggle notebook](https://www.kaggle.com/code/laingangiang2006/aud-usd-exchange-rate-analysis).

---

## Workflow & Key Steps

### 1. Install & Import Libraries
Installs and imports all required packages including `yfinance`, `pandas`, `matplotlib`, `seaborn`, `plotly`, `statsmodels`, and others.

### 2. Data Collection
- Prompts the user to enter a **currency pair** (e.g., `AUDUSD`) and a **date range**
- Downloads OHLCV data via **`yfinance`** and saves it locally as `currency.csv`
- Dataset: **1,688 rows**, zero missing values, columns: `Date`, `Close`, `High`, `Low`, `Open`, `Volume`

### 3. Exploratory Data Analysis (EDA)
- Summary statistics (`df.describe()`) — Close price ranges from **0.5743 to 0.7977**
- Missing value check (none found)
- **Line chart**: AUD/USD closing price over time (matplotlib + seaborn)
- **Yearly growth bar chart** (Plotly): % change per year from first to last close

### 4. Time Series Analysis
Decomposes the series to identify **trend**, **seasonality**, and **residual** components using `statsmodels` seasonal decomposition.

### 5. SARIMA Forecasting
- Fits a **SARIMA** model on the closing price series
- Forecasts the next **60 trading periods**
- Visualizes actual vs. predicted values with confidence intervals

---

## Technologies Used

| Tool | Purpose |
|---|---|
| Python 3.11 | Core programming language |
| Jupyter Notebook | Interactive development environment |
| yfinance 1.4.1 | Fetching historical exchange rate data |
| pandas 3.0.4 | Data manipulation |
| numpy 1.26.4 | Numerical computation |
| matplotlib 3.11.0 | Static visualizations |
| seaborn 0.13.2 | Statistical visualizations |
| plotly | Interactive charts (yearly growth) |
| statsmodels 0.14.6 | SARIMA time series modeling |
| scikit-learn 1.9.0 | Supporting utilities |

---

## Model

The notebook uses **SARIMA**, which extends ARIMA to capture **seasonal patterns** in the exchange rate time series. It first decomposes the series to detect trend and seasonality before fitting the model.

---

## Disclaimer

This project is for **educational purposes only** and should **not** be used as financial advice. Exchange rate forecasting is inherently uncertain.

---

## Author

**Lại Ngân Giang** — [GitHub Profile](https://github.com/laingangiang2006)
