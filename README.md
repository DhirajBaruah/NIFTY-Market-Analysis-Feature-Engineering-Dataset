# 📈 NIFTY Market Analysis & Feature Engineering Dataset

Welcome to the **NIFTY Market Feature Engineering** repository!

This project provides a feature-rich dataset derived from historical NIFTY index data collected from the **NSE (National Stock Exchange of India)**. The goal of this repository is to aid in **quantitative research**, **machine learning**, and **trading strategy development** by offering curated technical indicators, oscillators, and custom targets engineered from raw market data.

## 🗂️ Dataset Files

- `NIFTY.csv`: Raw historical data including:
  - `Day`: Date
  - `Advances`, `Declines`: Number of advancing/declining stocks
  - `Advance_Decline_Ratio`
  - `Open`, `High`, `Low`, `Close` prices

- `NIFTY_with_MultiClass_Targets.csv`: Cleaned and feature-enriched dataset with:
  - Engineered technical indicators
  - Market breadth metrics
  - Oscillators (Accelerator, Awesome Oscillator)
  - Custom binary and multi-class target variables for prediction

## ⚙️ Processing Workflow

The transformation process includes:

### ✅ 1. Target Engineering
- **Gap Target**: Binary label based on whether the next day's open shows a significant gap up.
- **5-Day Movement Target**: Multi-class label indicating price movement over the next 5 days.

### 📊 2. Technical Indicator Generation
- **Trend Indicators**: SMA, EMA, MACD
- **Momentum Indicators**: RSI, Stochastic %K
- **Volatility Indicators**: Bollinger Bands, ATR
- **Price Action**: Candle body size, high-low range, close position

### 🌐 3. Market Breadth Metrics
- Advance-Decline Ratio
- Advance-Decline Difference

### 🔁 4. Lag Features
- Lagged returns and breadth metrics for 1, 2, 3, and 5 days.

### 🧼 5. Cleanup
- Handled missing values due to rolling operations
- Final CSV file ready for modeling and analysis

## 📊 Sample Output

Sample columns from the final dataset include:
- `Day`, `Close`, `Gap`, `5d_Movement`, `Awosc`, `Acosc`
- Along with over **25+ engineered features** ready for ML applications

## 🤝 Contributing

We welcome **collaborators**, **data scientists**, and **quant enthusiasts** to:

- Propose new features or targets
- Perform exploratory data analysis (EDA)
- Apply machine learning models or backtesting strategies
- Share insights and visualizations

To contribute:
1. Fork the repository
2. Create your branch: `git checkout -b new-feature`
3. Commit your changes: `git commit -am 'Add something'`
4. Push to the branch: `git push origin new-feature`
5. Open a pull request

## 🧠 Possible Directions

- Building predictive models for gap-ups or 5-day movements
- Sentiment integration with price and breadth data
- Backtesting strategies using TA indicators
- Correlation and dimensionality reduction analysis

## 📌 Requirements

- `pandas`
- `numpy`
- `ta` (Technical Analysis library: [link](https://github.com/bukosabino/ta))

Install required Python libraries:

```bash
pip install pandas numpy ta
