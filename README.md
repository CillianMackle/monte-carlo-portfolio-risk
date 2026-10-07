# Monte Carlo Simulation of Portfolio Risk

An independent project developed in R to investigate portfolio risk using Monte Carlo simulation, Value at Risk (VaR), Expected Shortfall (ES), and stress testing.

## Project Overview

The analysis considers a £10,000 portfolio containing four publicly traded companies:

- Apple (30%)
- Microsoft (25%)
- JPMorgan Chase (25%)
- Johnson & Johnson (20%)

Historical stock prices from September 2021 to September 2026 were used to estimate expected returns, volatility, and correlations.

## Methodology

- Retrieved historical adjusted stock prices using the `quantmod` package in R.
- Estimated annualised returns and the covariance matrix.
- Generated 10,000 simulated one-year portfolio outcomes using Cholesky decomposition to preserve correlations.
- Calculated 95% VaR and Expected Shortfall.
- Conducted volatility and correlation stress tests.
- Simulated 500 portfolio value paths over 252 trading days.
- Investigated the Normal distribution assumption using Q-Q plots and kurtosis.

## Key Results

| Scenario | Volatility | VaR (95%) | ES (95%) |
|---|---|---|---|
| Original | 17.60% | £1,127 | £1,817 |
| Volatility Stress | 21.56% | £1,779 | £2,624 |
| Correlation Stress | 23.12% | £2,011 | £2,954 |

The results demonstrate how increased market volatility and stronger correlations between assets can significantly increase portfolio risk.

## Model Limitations

The simulation assumes multivariate Normally distributed returns and relies on historical estimates. Evidence of heavy tails in historical returns suggests that extreme losses may occur more frequently than the model predicts.

## Project Files

- `monte_carlo_portfolio.R` — Complete R analysis and visualisations.
- `Monte_Carlo_Portfolio_Risk_Report.pdf` — Full methodology, results, and discussion.
- `figures/` — Visualisations generated from the analysis.

## Tools

R, RStudio, quantmod, Monte Carlo simulation, Cholesky decomposition, statistical modelling, and data visualisation.
