# Stock Return and Volatility Analysis

A quantitative finance project analyzing historical asset returns, annualized volatility, cross-asset correlations, and volatility forecasting using econometric (GARCH) and machine learning (Random Forest) models.

## Overview
This repository provides an empirical examination of asset dynamics across major U.S. equities (Apple, Microsoft, JPMorgan Chase) relative to the benchmark S&P 500 index (`^GSPC`) from January 2019 to January 2024.

## Key Features
- **Data Collection:** Automated extraction and local caching of adjusted closing prices using `yfinance`.
- **Return & Risk Analysis:** Daily returns, annualized return, annualized volatility (252 trading days), and Sharpe ratios ($R_f = 2\%$).
- **Correlation Analysis:** Cross-asset correlation matrix of returns.
- **Econometric Modeling:** Fitted a GARCH(1,1) model for conditional volatility modeling and 1-day ahead volatility forecasting.
- **Machine Learning:** Implemented a Random Forest Regressor using lagged volatility features to predict future volatility.
- **Model Evaluation:** Evaluated machine learning forecast accuracy using Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE).

## Summary Results (2019–2024)

| Asset | Annualized Return (%) | Annualized Volatility (%) | Sharpe Ratio |
| :--- | :---: | :---: | :---: |
| **AAPL** | 37.80 | 31.81 | 1.11 |
| **MSFT** | 27.50 | 27.47 | 0.93 |
| **JPM** | 15.65 | 27.75 | 0.49 |
| **^GSPC** | 15.20 | 21.32 | 0.62 |

### Volatility Forecasting Performance (AAPL)
- **GARCH(1,1):** Next-day predicted volatility is approx. 1.13% (daily) / 17.89% (annualized).
- **Random Forest Regressor:**
  - **MAE:** 0.0089
  - **RMSE:** 0.0113

## Project Structure
- `data_and_returns.ipynb`: Complete Jupyter Notebook containing data pipeline, risk-return statistics, GARCH modeling, and ML implementation.
- `prices.csv`: Locally cached historical adjusted close prices.

## How to Run
1. Clone this repository:
```bash
   git clone https://github.com/Mohammadreza-Zolghadri/stock-return-volatility-analysis.git
   
