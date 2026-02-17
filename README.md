# Estimating a Risk Factor Model for a Stock with Live Data

An applied asset pricing project that estimates **Fama-French Carhart four-factor exposures** for publicly traded stocks using live market data in Python.

## Overview

This project implements a comprehensive workflow for estimating factor risk exposures on individual stocks. It combines the Fama-French research factors with live stock price data and performs regression-based beta estimation to understand how a stock's returns are driven by broad market factors.

### Factor Model Framework

The analysis uses the **Fama-French Carhart 4-Factor Model**, which extends the classic Fama-French 3-Factor Model:

- **Market Factor (Mkt-RF)**: Market excess return over the risk-free rate
- **Size Factor (SMB)**: Small Minus Big - the premium from small-cap vs. large-cap stocks
- **Value Factor (HML)**: High Minus Low - the premium from high book-to-market vs. low book-to-market stocks
- **Momentum Factor (Mom)**: The return momentum effect on stock prices

## Project Workflow

### 1. **Data Sourcing**
- Retrieves **Fama-French factor returns** using `pandas_datareader` from Kenneth French's data library
- Accesses **historical stock price data** via `yfinance`
- Collects data from 1926 onwards with monthly frequency

### 2. **Data Processing**
- Merges factor data with individual stock returns
- Constructs **excess returns** (stock return minus risk-free rate)
- Handles missing data and aligns time series properly

### 3. **Beta Estimation**
- Performs **OLS regression analysis** to estimate factor exposures
- Calculates sensitivity coefficients for each risk factor
- Evaluates statistical significance and model fit (R², adjusted R²)

### 4. **Analysis & Visualization**
- Visualizes factor returns and stock performance over time
- Plots rolling average factor returns (6-year windows)
- Displays regression results and residual analysis

## Key Libraries

```python
pandas_datareader  # Retrieve Fama-French factors
yfinance           # Download historical stock prices
pandas             # Data manipulation and analysis
numpy              # Numerical computations
matplotlib         # Visualization
sklearn            # Statistical modeling
