# Market Regime Detection and Dynamic Portfolio Allocation

## Overview

This project explores whether financial market environments can be grouped into distinct **market regimes** and whether those regimes can be used to improve **portfolio allocation decisions**.

The project uses a combination of:
- **Unsupervised learning** to detect market regimes
- **Supervised learning** to predict future regimes
- **Regime-based portfolio backtesting** to evaluate investment performance relative to static benchmarks

This project was developed as part of the **University of Michigan Master of Applied Data Science (MADS) Capstone (SIADS 699)**.

---

## Project Objective

Financial markets do not behave the same way over time. Periods of calm, transition, and stress can lead to very different return and risk patterns across asset classes.

The objection of this project is to:
1. Detect distinct market regimes using historical financial data
2. Predict the next market regime using supervised machine learning
3. apply predicted regimes to a portfolio allocation strategy
4. comapre the strategy aginst benchmark allocation such as **SPY buy-and-hold**

__

## Data Source

This project uses publicly available financial data from the following sources:

### Narket Data
-**Hahoo Finance** (via 'yfinance')
- Examples: SPY, QQQ, LTL, GLD< sector ETFs, global indices, and VIX-related series

### Macreconomic Data
-**FRED (Federal Reserve Economic Data)** (via 'fredapi')
- Examples: 10-Year Treasury Yield, 2-Year Treasury Yield

--
