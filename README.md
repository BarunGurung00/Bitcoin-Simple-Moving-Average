# Bitcoin-Simple-Moving-Average

# Simple Moving Average (SMA) Crossover Strategy & Backtester

A robust quantitative finance project implementing a **Trend-Following (Momentum) Strategy** using Simple Moving Average (SMA) crossovers on historical asset prices (defaulting to Bitcoin via Yahoo Finance). 

This project explores technical analysis, parameter optimization, and performance backtesting using Python, Pandas, and interactive plotting tools.

---

## 🚀 Key Features
- **Data Acquisition:** Automatically downloads historical OHLCV (Open, High, Low, Close, Volume) data using `yfinance`.
- **SMA Crossover Engine:** Configurable leading (short-term) and lagging (long-term) moving averages with custom trigger thresholds.
- **Long/Short Positioning:** Dynamically generates trading signals (1 for Long, -1 for Short, 0 for Flat) based on price momentum.
- **Parameter Grid Search & Heatmaps:** Tests combinations of lead/lag parameters across historical data to evaluate performance differences (PnL) visually using Seaborn heatmaps.
- **Performance Tearsheets:** Integrates with `pyfolio` for advanced strategy metrics and risk analysis.

---

## 🛠️ Tech Stack & Libraries
- **Language:** Python 3.x
- **Data Manipulation:** `pandas`, `numpy`
- **Financial Data:** `yfinance`
- **Performance & Metrics:** `pyfolio-reloaded`
- **Visualization:** `matplotlib`, `seaborn`, `plotly`, `altair`

---

## 📊 Strategy Logic
The strategy uses two moving averages to capture market trends:
1. **Leading SMA (Short-term):** More sensitive to recent price movements.
2. **Lagging SMA (Long-term):** Slower to react, establishing the broader baseline trend.

* **LONG:** Triggered when the Leading SMA crosses above the Lagging SMA by a defined percentage threshold.
* **SHORT:** Triggered when the Leading SMA crosses below the Lagging SMA by the threshold.

---

## ⚙️ How to Run
1. Open the notebook in **Google Colab** or your local Jupyter environment.
2. Run the initialization block to load all required helper functions and dependencies (`yfinance`, `pyfolio`, etc.).
3. Adjust your backtesting parameters (e.g., `ticker`, `startDate`, `lead`, `lag`, and `threshold`).
4. Execute the cells sequentially to view exploratory charts, strategy performance curves, and optimization heatmaps.

---

## 💡 Future Enhancements / Suggestions
- Experiment with alternative technical indicators such as RSI (Relative Strength Index) or Bollinger Bands.
- Split historical datasets into separate **Research** and **Backtest** portions to prevent overfitting during parameter tuning.
- Test the strategy on alternative asset classes (e.g., equities or forex pairs).
