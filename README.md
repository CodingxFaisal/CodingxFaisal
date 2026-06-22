# Mohammad Faisal

Power engineer (M.Sc., Renewable Energy) working at the intersection of energy
markets, storage, and data. I build reproducible models and backtests on real
European market data to answer practical questions: what a battery is actually
worth, when a trading signal is real, and how renewables reshape the prices they
depend on.

**Focus areas:** power markets (day-ahead and intraday), battery storage
economics, optimization (MILP), time-series forecasting, and market analytics.

**Toolbox:** Python, pandas, NumPy, scikit-learn, PuLP, matplotlib, seaborn,
Streamlit.

---

## Selected projects

All three run end to end on real, free German market data from
[SMARD.de](https://www.smard.de/en), come with tests, and document their
assumptions.

| Project | What it does | Headline result |
|---|---|---|
| [BESS Day-Ahead Dispatch Optimizer](https://github.com/CodingxFaisal/bess-dispatch-optimizer) | MILP optimization of a grid-scale battery trading day-ahead arbitrage | A gradient-boosting price forecast captures **84.5%** of the perfect-foresight revenue ceiling |
| [Power Spread Trader](https://github.com/CodingxFaisal/power-spread-trader) | Backtest of a cross-border spread mean-reversion strategy, with an honest test of whether the edge is real and realizable | Out-of-sample **Sharpe 5.45**, bounded by tradability rather than cost |
| [Renewable Price Cannibalization](https://github.com/CodingxFaisal/renewable-cannibalization) | Analysis and dashboard of how solar and wind erode their own market value | Solar value factor falls from **0.93 (2019) to 0.59 (2024)** |

### BESS Day-Ahead Dispatch Optimizer

A grid-scale battery scheduled against real German day-ahead prices with a
mixed-integer program (PuLP/CBC), covering round-trip efficiency, a daily cycle
budget, and a derived degradation cost. The project measures how much revenue
survives once perfect foresight is replaced by an actual price forecast, and adds
a duration sweep and a walk-forward, no-lookahead backtest.
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

---

## Contact

- Email: mohammad.faisal@gmx.de
- GitHub: [github.com/CodingxFaisal](https://github.com/CodingxFaisal)

*Market data throughout is published by SMARD.de / Bundesnetzagentur and used
under their terms.*
