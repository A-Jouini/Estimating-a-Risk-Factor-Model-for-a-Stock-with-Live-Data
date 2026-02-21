# Equity Risk Factor Model (Live Data + Diagnostics)

## Overview
This project estimates a **risk factor model** for a single stock using live market data and factor returns.  
It focuses on **interpretable risk attribution** rather than prediction hype.

Core questions:
- How much of a stock’s return is explained by **systematic factors**?
- Are exposures stable over time (**rolling beta**)?
- What portion of risk is **idiosyncratic** vs **systematic**?

## What’s Inside
- **Live data pull**: stock returns + factor data
- **Factor regression** (OLS)
  - CAPM-style market beta and multi-factor extensions (where applicable)
- **Diagnostics**
  - Residual checks (basic sanity tests)
  - Rolling beta (time-varying exposure)
  - Variance decomposition: systematic vs idiosyncratic
  - Simple out-of-sample validation (fit early period, evaluate later)

## Key Enhancements (Iteration Notes)
Recent improvements focus on “institutional-style” risk work:
- Added **rolling beta** to show exposure changes over time
- Added **residual diagnostics** to check model misspecification
- Added **variance decomposition** for risk attribution
- Added a **simple OOS check** to avoid purely in-sample conclusions

## How to Run
1. Open the notebook in Google Colab
2. Run cells top-to-bottom
3. Optional: switch ticker, extend window, or compare exposures across stocks

## Repository Structure
- `*.ipynb` — main research notebook
- `README.md` — project overview

## Notes / Disclaimer
This is for educational and research purposes only. It is not investment advice.
Factor models are simplified approximations and can break in different regimes.
