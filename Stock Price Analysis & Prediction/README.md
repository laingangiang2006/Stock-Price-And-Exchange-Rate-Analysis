# AAPL Stock Price Prediction using LSTM

A time series deep learning project analyzing and forecasting Apple (AAPL) stock closing prices using historical OHLCV data with an LSTM neural network.

---

## Overview

This notebook analyzes the historical Apple (AAPL) stock price and builds an **LSTM (Long Short-Term Memory)** neural network to forecast future closing prices. The model is trained on a user-specified historical period and evaluated on a held-out validation set using RMSE.

---

## Workflow & Key Steps

### 1. Install & Import Libraries

Installs and imports all required packages including `yfinance`, `pandas`, `numpy`, `matplotlib`, `scikit-learn`, `tensorflow`, and `neuralprophet`.

### 2. Data Collection
- Prompts the user to enter a **stock ticker** (e.g., `AAPL`) and a **date range**
- Downloads OHLCV data via **`yfinance`** and saves it locally as `stock_data.csv`
- Checks dataset shape, structure (`df.info()`), and missing values

### 3. Exploratory Data Analysis (EDA)
- **Line chart**: Closing price over time
- **Moving averages**: MA20, MA50, MA200 plotted against the closing price
- **Volume chart**: Daily trading volume
- **Daily return**: Percentage change in closing price, plotted over time
- **Volatility**: Distribution of daily returns (histogram)
- **Cumulative return**: Compounded return over the full period

### 4. Data Preprocessing
- Splits data into **training (80%)** and **validation (20%)** sets
- Scales closing prices to a [0, 1] range using `MinMaxScaler`
- Builds sliding-window sequences (45-day lookback) for supervised learning

### 5. LSTM Model Training
- Builds a stacked **LSTM** network with Dropout regularization and Dense output layers
- Trains the model using the Adam optimizer and Mean Squared Error loss

### 6. Results & Evaluation
- Computes **RMSE** on the validation set
- Visualizes actual vs. predicted closing prices
- Plots full training/validation/prediction timeline

---

## Technologies Used

| Tool | Purpose |
|---|---|
| Python | Core programming language |
| Jupyter Notebook | Interactive development environment |
| yfinance | Fetching historical stock data |
| pandas | Data manipulation |
| numpy | Numerical computation |
| matplotlib | Visualizations |
| scikit-learn | Data scaling (MinMaxScaler) |
| TensorFlow / Keras | LSTM model building & training |
| NeuralProphet | Imported for alternative forecasting |

---

## Disclaimer

This project is for **educational purposes only** and should **not** be used as financial advice. Stock price forecasting is inherently uncertain.

---

## Author

**Your Name** — [GitHub Profile](https://github.com/your-username)
