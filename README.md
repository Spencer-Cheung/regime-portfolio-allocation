# Market Regime Detection and Dynamic Portfolio Allocation

## Overview

This project explores whether financial market environments can be grouped into distinct **market regimes** and whether those regimes can be used to improve **portfolio allocation decisions**.

The project uses a combination of:
- **Unsupervised learning** to detect market regimes
- **Supervised learning** to predict future regimes
- **Regime-based portfolio backtesting** to evaluate investment performance relative to static benchmarks

This project was developed as part of the **University of Michigan Master of Applied Data Science (MADS) Capstone (SIADS 699)**.



## Project Objective

Financial markets do not behave the same way over time. Periods of calm, transition, and stress can lead to very different return and risk patterns across asset classes.

The objective of this project is to:
1. Detect distinct market regimes using historical financial data  
2. Predict the next market regime using supervised machine learning  
3. Apply predicted regimes to a portfolio allocation strategy  
4. Compare the strategy against benchmark allocations such as **SPY buy-and-hold**


## Data Source

This project uses publicly available financial data from the following sources:

### Market Data
- **Yahoo Finance** (via 'yfinance')
- Examples: SPY, QQQ, TLT, GLD, sector ETFs, global indices, and VIX-related series

### Macroeconomic Data
- **FRED (Federal Reserve Economic Data)** (via 'fredapi')
- Examples: 10-Year Treasury Yield, 2-Year Treasury Yield

**All data used in this project is publicly accessible and does not require special permissions.**  
**Users must provide their own FRED API key to access macroeconomic data.**

No proprietary or restricted datasets are included in this repository.


## Methodology

The project is organized into three main steps:

### 1. Unsupervised Learning: Market Regime Detection
We engineer volatility, return, and macroeconomic features from historical weekly market data and use clustering methods to identify distinct market regimes.

### 2. Supervised Learning: Regime Prediction
After labeling the historical data with regimes, we train supervised machine learning models to predict the **next period’s regime** using lagged financial and macroeconomic features.

### 3. Portfolio Backtesting
Predicted regimes are used to drive dynamic portfolio allocations across a selected set of assets. Strategy performance is then compared with benchmark portfolios using return, volatility, Sharpe ratio, and drawdown metrics.


## Repository Structure

```text
.
├── README.md
├── requirements.txt
├── data/
│   └── (optional local data files if used)
├── notebooks/
│   ├── 01_data_collection.ipynb
│   ├── 02_feature_engineering.ipynb
│   ├── 03_unsupervised_regime_detection.ipynb
│   ├── 04_supervised_regime_prediction_1_stage.ipynb
│   ├── 05_supervised_regime_prediction_2_stage.ipynb
│   ├── 06_supervised_regime_prediction_combined.ipynb
│   ├── 07_portfolio_backtest_Unsupervised.ipynb
│   ├── 08_portfolio_backtest_Supervised.ipynb
│   └── 09_portfolio_backtest_2_layer.ipynb
│   └── 10_portfolio_backtest_Combined.ipynb
├── src/
│   └── (optional helper scripts / functions)
└── figures/
    └── (generated charts used in report)
```

## How to Run This Project

This project can be run either locally using Jupyter Notebook or through Deepnote.

# please use your own FredAPI Key

#### 1. Clone the repository

```bash
git clone https://github.com/Spencer-Cheung/regime-portfolio-allocation.git
cd regime-portfolio-allocation
```

#### 2. Install dependencies

```bash
pip install -r requirements.txt
```

#### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```
