# Stock Return and Volatility Analysis

A quantitative finance project analyzing historical asset returns, annualized volatility, cross-asset correlations, and risk-adjusted performance using daily market data (2019–2024).

## Overview
This repository provides an empirical examination of asset dynamics across major U.S. equities (Apple, Microsoft, JPMorgan Chase) relative to the benchmark S&P 500 index (`^GSPC`).

## Key Methodologies
- **Daily Returns:** Tracking day-over-day price adjustments using percentage change.
- **Annualized Risk Metrics:** Scaled by $\sqrt{252}$ trading days to compute historical annual volatility.
- **Sharpe Ratio Estimation:** Assessing excess return relative to risk under a 2% baseline risk-free rate.
- **Correlation Matrix Analysis:** Evaluating asset co-movements and diversification potential.

## Summary Results (2019 - 2024)
| Ticker | Annualized Return (%) | Annualized Volatility (%) | Sharpe Ratio |
| :--- | :---: | :---: | :---: |
| **AAPL** | 37.80% | 32.23% | 1.11 |
| **MSFT** | 32.03% | 30.49% | 0.98 |
| **JPM**  | 18.90% | 31.90% | 0.53 |
| **^GSPC** | 15.16% | 21.32% | 0.62 |

## Requirements
```bash
pip install numpy pandas matplotlib yfinance
