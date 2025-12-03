A python-based portfolio optimisation tool. This notebook builds a long-only, Sharpe-ratio–maximized portfolio over a small universe of ETFs using historical data and classical mean–variance techniques.

The portfolio universe is defined as:

tickers = ["SPY", "QQQ", "BND", "GLD", "VTI"]

We query the FRED API for the 10-year Treasury yield and treat that as the risk-free rate.
We pull ~5 years of daily closing prices for each ETF and compute daily log returns.
From these, we estimate the annualized covariance matrix of returns

We then define helper functions to compute Portfolio standard deviation (volatility), expected retuns and the sharpe ratio.

Finally, we print:
Optimal weights for each ticker
Expected annual return of the optimal portfolio
Annualized volatility (standard deviation)
Sharpe ratio


The notebook demonstrates:
Calculation of expected returns & covariance matrices
Mean–variance optimization to generate efficient portfolios
Maximization of the Sharpe ratio (risk-adjusted returns)
