---
layout: post
title: Investment Strategy Evaluation
---

This post collects backtest statistics and investment metrics I have learned over the years which I used to evaluate investment strategies. A link to this Jupyter Notebook shows the implementations with Python with NumPy and Pandas.

### General Characteristics
- Time Range
- Average AUM
- Capacity
- Leverage
- Maximum Dollar Position
- Ratio of Longs
- Frequency of Bets
- Average Holding Period
- Annualized Turnover
- Correlation to Underlying

### Performance Metrics
- PnL
- PnL from Long Positions
- Annualized Rate of Return
Time-Weighted Rate of Return
- Average Return from Hits
- Average Return from Misses

### Run
- Returns Concentration
  - High sharpe ratio
  - High number of bets per year
  - High hit ratio
  - No fat tail
  - Bets are not concentrated in time
 - Drawdown and Time under Water
 - Runs Statistics for Performance Evaluation
  - HHI index on positive returns
  - HHI index on negative returns
  - HHI index on time between bets
  - 95-percentile DD
  - 95-percentile TuW
 
### Implementation Shortfall
 - Broker fees per turnover
 - Average slippage per tunrover
 - Dollar performance per turnover
 - Return on execution costs
 
### Efficiency
 - Sharpe Ratio
 - Probabilistic Sharpe Ratio
 - Deflated Sharpe Ratio
 - Information Ratio
 
### Classification Score
 - Accuracy
 - Precison
 - Recall
 - F1 Score
 - Negative log-loss
 
### Attribution
 - Barra's multi-factor

### Risk Metric
- Volatility Risk
 - Standard Deviation
 - Downside Deviation
 - Sharpe Ratio
 - Sortino Ratio
- Benchmark Risk
  - Excess Return
  - Batting Average
  - Up Capture
  - Down Capture
  - Alpha
  - Beta
  - R-squared
  - Tracking Error
  - Treynor Ratio
  - Information Ratio
  - M-squared
- Capital Preservation Risk
  - Maximum Drawdown
  - Pain Ratio (Pain Index)
  - Calmar Ratio
- Tail Risk
  - Skewness
  - Kurtosis
  - Omega
  - VaR
  - CVaR
