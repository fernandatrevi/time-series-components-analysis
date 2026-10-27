# Time Series Components Analysis

Course-based analysis of three datasets: annual automobile and motorcycle registrations in Nuevo León, and daily sales at Rossmann Store 1.

## Research questions
- Is there a visible trend?
- What patterns appear in the autocorrelation function (ACF)?
- What do ADF and KPSS indicate about stationarity?
- What is the dominant spectral period (L), and is seasonality supported?

## Methods
The analysis follows the supplied course notebook `S11_Time_Series_Components (1).ipynb`. It uses `pandas.read_excel`, `matplotlib.pyplot.plot`, `statsmodels.graphics.tsaplots.plot_acf`, `statsmodels.tsa.stattools.adfuller`, `statsmodels.tsa.stattools.kpss` with `regression="ct"`, and `scipy.signal.periodogram`. No forecasting models are introduced.

## Results
| Dataset | ADF p | KPSS p (trend) | Dominant L |
|---|---:|---:|---:|
| Automobiles, Nuevo León | 0.0852 | 0.0138 | 37 years |
| Motorcycles, Nuevo León | 0.9986 | ≥ 0.10 (table bound) | 17 years |
| Rossmann Store 1 | 0.0226 | ≥ 0.10 (table bound) | ≈365.2 days |

ADF has a unit-root null; KPSS with `regression="ct"` has a trend-stationarity null. A dominant periodogram peak does not by itself establish seasonality. See `docs/` for series-specific interpretations.

## Repository structure
- `notebooks/`: class-method analysis
- `data/`: original Excel datasets
- `figures/`: nine diagnostic charts
- `docs/`: methodology, interpretations, and reproducibility notes

## Running
Install dependencies with `pip install -r requirements.txt`, open the notebook, and run its cells after placing the Excel files in `data/`.

**Upload status:** The Excel datasets and PNG figures are pending binary upload. Results are reported from the supplied analysis; full independent reproduction requires the original datasets.
