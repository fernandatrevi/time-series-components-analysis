# Methodology

Annual years are parsed using `pd.to_datetime(year.astype(str), format='%Y')`; Rossmann dates are daily. Series are sorted chronologically. Line charts show direction; `plot_acf` shows lag correlation; `adfuller(..., autolag='AIC')` tests the unit-root null; `kpss(..., regression='ct', nlags='auto')` tests trend stationarity. `periodogram` identifies a dominant nonzero frequency, with L = 1 / frequency. A low-frequency peak can reflect slow movement rather than a recurring cycle.
