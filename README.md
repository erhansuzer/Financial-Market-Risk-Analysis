# Financial Market Risk & Return Analysis

A quantitative data analysis script designed to evaluate historical price behavior, volatility, and downside risk metrics across equities using time-series market data.

## Overview
The goal of this project is to model risk-adjusted performance rather than relying solely on raw price returns. The analysis extracts adjusted market data, calculates momentum and volatility indicators, and maps the comparative risk profile of selected assets.

## Core Metrics & Methodology
* **Data Processing:** Historical daily price series fetched via `yfinance` with split and dividend adjustments applied. Missing trading days handled through forward-filling.
* **Return Metrics:** Daily percentage changes calculated alongside continuous cumulative returns.
* **Trend & Volatility:** 20-day and 50-day Simple Moving Averages (SMA) implemented for momentum tracking; 21-day annualized rolling volatility computed using square-root-of-time scaling ($\sqrt{252}$).
* **Downside Risk:** Peak-to-trough series formulated to calculate Maximum Drawdown (MDD).
* **Risk-Adjusted Return:** Annualized Sharpe Ratio evaluated across all assets to compare excess return per unit of total risk.

## Visualizations

### Price Trend & Drawdown Dynamics
Historical price action plotted against moving averages, paired with continuous drawdown depths.

![Trend and Drawdown](thyao_analysis.png)

### Risk vs. Return Distribution
Cross-sectional comparison mapping annualized volatility against annualized return, with Sharpe ratio markers.

![Risk vs Return Scatter](risk_return_scatter.png)

## Dependencies
* Python 3.x
* pandas
* numpy
* matplotlib
* yfinance

## Usage
Open and run `market_risk_analysis.ipynb` in any Jupyter Notebook environment or Google Colab to reproduce the tables and plots.
