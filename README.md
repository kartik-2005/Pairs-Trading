#  Pairs Trading Strategy using Cointegration (NSE Stocks)

This repository implements a **Pairs Trading Strategy** using statistical arbitrage techniques like **cointegration tests**, **z-score thresholding**, and **long-short portfolio backtesting**. The project is applied to NSE-listed IT sector stocks and analyzes their historical performance.

## 📈 Project Overview

- **Goal**: Identify cointegrated stock pairs and exploit mean-reverting behavior for profitable trades.
- **Sector**: Indian IT Sector (NSE)
- **Period**: 2019-04-01 to 2025-03-31
- **Backtest Capital**: ₹100,000

### 🔍 Key Features

- Download & preprocess historical stock data using `yfinance`
- Identify cointegrated pairs using Engle-Granger test
- Confirm stationarity of the spread via ADF test
- Construct dynamic z-score based entry/exit signals
- Backtest individual pairs and overall portfolio
- Visualize performance: portfolio curve, drawdown, z-score, PnL, and positions
- Evaluate metrics: Sharpe Ratio, Win Rate, Max Drawdown, Total Return

---

## 🛠️ Tech Stack

| Tool/Library     | Purpose                                |
|------------------|----------------------------------------|
| `Python`         | Core programming language              |
| `yfinance`       | Downloading historical stock prices    |
| `pandas`         | Data manipulation                      |
| `numpy`          | Numerical operations                   |
| `statsmodels`    | Cointegration & ADF tests              |
| `matplotlib`     | Visualizations                         |
| `seaborn`        | Enhanced plotting aesthetics           |
| `scikit-learn`   | Optional clustering (future expansion) |

---

## 🧪 How It Works

1. **Data Loading**  
   Download adjusted close prices using `yfinance`.

2. **Pair Selection**  
   - Compute pairwise cointegration via Engle-Granger method
   - Filter on high correlation and ADF stationarity of spread

3. **Backtesting**  
   - Calculate rolling z-score of spread
   - Trade when z-score crosses entry/exit thresholds
   - Long/Short the pair based on mean-reversion assumption

4. **Performance Analysis**  
   - Evaluate strategy return, drawdown, Sharpe ratio
   - Visualize trades, PnL, portfolio value, drawdowns

---
