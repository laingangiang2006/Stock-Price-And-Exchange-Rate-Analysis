# AUD-USD Exchange Rate Analysis & Prediction

A time series data science project analyzing and forecasting the AUD/USD exchange rate using historical OHLCV data (2020–2026) with SARIMA modeling.

---

## Overview

This notebook analyzes the historical AUD/USD exchange rate and builds a **SARIMA (Seasonal AutoRegressive Integrated Moving Average)** forecasting model to predict future exchange rates for the next **60 trading periods**. The analysis covers data from **January 2020 to June 2026** (1,688 trading days).

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

## Getting Started

### Prerequisites

Python 3.8+ recommended. Install all dependencies with:

```bash
pip install yfinance pandas matplotlib numpy scikit-learn seaborn statsmodels plotly nbformat
```

### Running the Notebook

1. Clone the repository:
   ```bash
   git clone https://github.com/laingangiang2006/Stock-Price-And-Exchange-Rate-Analysis.git
   ```

2. Navigate to the project folder:
   ```bash
   cd "Stock-Price-And-Exchange-Rate-Analysis/AUD-USD Exchange Rate Analysis & Prediction"
   ```

3. Launch Jupyter:
   ```bash
   jupyter notebook
   ```

4. Open `AUDUSD_Exchange_Rate_Analysis_SARIMA.ipynb` and run all cells.

5. When prompted, enter:
   - **Currency Pair**: `AUDUSD`
   - **Start date**: `2020-01-01`
   - **End date**: `2026-06-28` (or yesterday's date)

---

## Model

The notebook uses **SARIMA**, which extends ARIMA to capture **seasonal patterns** in the exchange rate time series. It first decomposes the series to detect trend and seasonality before fitting the model.

---

## Disclaimer

This project is for **educational purposes only** and should **not** be used as financial advice. Exchange rate forecasting is inherently uncertain.

---

## Author

**Lại Ngân Giang** — [GitHub Profile](https://github.com/laingangiang2006)

---

This README is based directly on the contents of your uploaded notebook. Let me know if you'd like to tweak any section!
