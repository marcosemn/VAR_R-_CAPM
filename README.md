# CAPM and VAR for a Brazilian ESG Equity Portfolio

Study in R of how a Brazilian ESG equity portfolio relates to the market, combining a CAPM regression with time-series tests.

## Steps

1. Test stationarity with the Augmented Dickey-Fuller test and difference the series where needed.
2. Select the lag order and estimate a VAR model for portfolio and market returns.
3. Estimate the CAPM by OLS: portfolio return on market return.
4. Run Granger causality tests in both directions.

## Results

| Test | Result |
|---|---|
| CAPM beta | 0.67 (t = 32.6) |
| CAPM alpha | 0.037, not significant (p = 0.21) |
| Market → portfolio (Granger) | F = 28.7, significant |
| Portfolio → market (Granger) | F = 1.18, p = 0.31, not significant |

The portfolio moves less than the market (beta below 1), shows no significant abnormal return, and market returns help predict the portfolio's but not the reverse. Full tables in `Results.png`.

## Files

- `Coding.txt`: R script (tseries, vars, lmtest, forecast, nortest)
- `Base_de_dados_ESG_dadosdiários.xlsx`: data
- `Results.png`: estimation tables
