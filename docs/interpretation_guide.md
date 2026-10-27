# Interpretation guide

**Trend**: describe the direction visible in the line plot.

**ADF**: null hypothesis is a unit root; a small p-value rejects that null.

**KPSS with `regression='ct'`**: null hypothesis is stationarity around a deterministic trend; a small p-value rejects it.

**Conflicting results**: do not force a definitive stationarity claim.

**Periodogram**: L = 1 / dominant frequency, expressed in observations. The highest spectral peak may reflect long-run changes rather than seasonality.

**KPSS p = 0.10**: this may be a lookup-table boundary, not an exact p-value.
