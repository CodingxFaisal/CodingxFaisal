# Mohammad Faisal

### Energy Systems Engineer · Optimization, Forecasting & Techno-Economic Modeling

Power engineer (M.Sc.) working at the intersection of energy markets, storage,
and data. I build reproducible models and backtests on real European market data
to answer practical questions: what a battery is actually worth, when a trading
signal is real, and how renewables reshape the prices they depend on.

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white)
![Optimization](https://img.shields.io/badge/Optimization-LP%2FMILP-2E7D32)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?logo=streamlit&logoColor=white)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mohdfaisal0412)
[![Email](https://img.shields.io/badge/Email-mohammad.faisal%40gmx.de-EA4335?logo=gmail&logoColor=white)](mailto:mohammad.faisal@gmx.de)

**Focus areas:** power markets (day-ahead and intraday), battery storage
economics, optimization (MILP), PV and renewable modelling, price forecasting,
and market analytics.

**Toolbox:** Python, pandas, NumPy, scikit-learn, PuLP, HiGHS, pvlib, FastAPI,
matplotlib, seaborn, Streamlit.

---

## Selected projects

All five run end to end on real, free European data (mainly
[SMARD.de](https://www.smard.de/en) and PVGIS), come with tests, and document
their assumptions.

| Project | What it does | Headline result |
|---|---|---|
| [GridFlex: BESS Dispatch & Day-Ahead Market Research](https://github.com/CodingxFaisal/bess-dispatch-optimizer) | Reproducible battery dispatch optimisation (MILP) and leakage-safe backtesting on the German day-ahead market | Trained price forecasts capture **83–84%** of perfect-foresight revenue over a 639-day hold-out |
| [Power Spread Trader](https://github.com/CodingxFaisal/power-spread-trader) | Backtest of a cross-border spread mean-reversion strategy, with an honest test of whether the edge is real and realizable | Out-of-sample **Sharpe 5.45**, bounded by tradability rather than cost |
| [Renewable Price Cannibalization](https://github.com/CodingxFaisal/renewable-cannibalization) | Analysis and dashboard of how solar and wind erode their own market value | Solar value factor falls from **0.93 (2019) to 0.59 (2024)** |
| [PV Market Value](https://github.com/CodingxFaisal/pv-market-value) | Values PV plant designs against day-ahead prices, comparing energy yield with revenue | A single-axis tracker earns **~15% more revenue** than the yield-optimal fixed array |
| [Day-Ahead Price Forecasting Service](https://github.com/CodingxFaisal/day-ahead-forecast-service) | A forecasting service with a full predict-score-retrain loop (FastAPI) | Day-ahead price forecast at about **6-7 EUR/MWh** mean absolute error |

### GridFlex: BESS Dispatch & Day-Ahead Market Research

A 10 MW / 20 MWh battery traded on the German day-ahead market, from raw SMARD
data to a financial result. Price forecasts (persistence, seasonal naive,
LEAR-style Lasso, gradient boosting) use only information published before the
12:00 gate closure, enforced by publication-time guards and tested. A
mixed-integer program (PuLP + HiGHS) builds each day's schedule, which is
independently checked against the battery's physics and settled at the prices
that actually cleared. On a 2024–2025 hold-out, forecast-driven dispatch earns
**83–84%** of the perfect-foresight benchmark versus 43% for a simple heuristic.
Includes finance and sensitivity analysis, a Streamlit viewer, 452 tests in CI,
and a from-scratch reproduction that matched every result exactly.
→ [Repository](https://github.com/CodingxFaisal/bess-dispatch-optimizer)

### Power Spread Trader

A backtesting framework for a mean-reversion strategy on cross-border day-ahead
spreads. The strategy is intentionally simple; the focus is a rigorous
evaluation: no-lookahead accounting, a shuffled-data null test, a
parameter-stability check, transaction costs, and a strict out-of-sample split.
It finds a real signal and then explains why the realizable edge is limited by
transmission rights and liquidity.
→ [Repository](https://github.com/CodingxFaisal/power-spread-trader)

### Renewable Price Cannibalization

Six years of German generation, load, and price data used to quantify renewable
value factors, the merit-order slope (with the gas-price regime removed),
negative-price hours, a curtailment proxy, and revenue impact, plus an
interactive Streamlit dashboard.
→ [Repository](https://github.com/CodingxFaisal/renewable-cannibalization)

### PV Market Value

A pvlib model that simulates a PV plant's hourly output and values each design
(fixed orientation, east-west, single-axis tracker) against real German
day-ahead prices. It shows the revenue-optimal design is not the yield-optimal
one, because prices move with the sun: a tracker wins on both energy and captured
price, while facing west does not pay for a fixed array.
→ [Repository](https://github.com/CodingxFaisal/pv-market-value)

### Day-Ahead Price Forecasting Service

A day-ahead price forecaster served as a small service with a full machine-
learning loop: predict, store every forecast, score it against the actual prices
once they settle, and retrain only when the new model genuinely wins. Built with
FastAPI, scikit-learn, and SQLAlchemy.
→ [Repository](https://github.com/CodingxFaisal/day-ahead-forecast-service)

---

## Contact

- Email: mohammad.faisal@gmx.de
- LinkedIn: [linkedin.com/in/mohdfaisal0412](https://www.linkedin.com/in/mohdfaisal0412)
- GitHub: [github.com/CodingxFaisal](https://github.com/CodingxFaisal)

*Market data throughout is published by SMARD.de / Bundesnetzagentur and used
under their terms.*
