# Forecasting Nominal Broad Dollar Index

Time series forecast of the Nominal Broad Dollar Index (NBDI) using ARIMA, built in R.

## Data
- Source: [FRED - DTWEXBGS](https://fred.stlouisfed.org/series/DTWEXBGS)
- Range: March 2015 - October 2024
- Train: Mar 2015 - Feb 2024 (110 obs) | Test: May 2024 - Oct 2024 (6 obs)

## Method
1. Checked stationarity — data showed clear upward trend, no need for variance transform (Box-Cox λ ≈ 1).
2. Differenced once at lag 1 to remove trend (lowest variance vs. seasonal differencing).
3. Used ACF/PACF to bound candidate p, q values, then selected model by lowest AICc.
4. Validated residuals (Shapiro-Wilk, Box-Pierce, Ljung-Box, McLeod-Li) — all passed, residuals resemble white noise.
5. Forecasted final 6 months and compared against test set.

## Final Model
**ARIMA(2,1,2)**

```
Yt = 0.7119·Yt−1 − 0.8342·Yt−2 + Zt + 0.438·Zt−1 + 0.7085·Zt−2
```

## Result
Strong predictive accuracy against the test set, though prediction intervals were wide.

## Requirements
`tidyverse`, `tidyquant`, `knitr`, `imputeTS`, `MASS`, `astsa`, `forecast`

## Author
Cyrus Navasca — thanks to Dr. Raya Feldman for guidance.
