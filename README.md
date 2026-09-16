# Portfolio Backtesting and Dollar Cost Averaging (DCA) Simulation

This repository contains the Python scripts used to perform a quantitative **backtesting** analysis of a personal investment portfolio. The primary goal is to demonstrate the statistical effectiveness of the **Dollar Cost Averaging (DCA)** strategy against a single **Lump Sum** investment over a volatile period (2020–2025).

As an **Economist and Data Scientist**, the methodology prioritizes **evidence-based decision-making** and risk management over market timing.

## Key results

| Scenario | Total Invested | Final Portfolio Value | Return (%) |
| :--- | :--- | :--- | :--- |
| A (Lump Sum) | $5,000 | $13,652 | 173.0% |
| B (DCA Monthly) | $15,000 | **$29,003** | 93.4% |

**Finding:** Although the Lump Sum had a higher percentage return (it entered near the 2020 market bottom), the **DCA strategy yielded 112% more absolute capital** ($29,003 vs. $13,652). That matters for an investor who funds the account with a stable monthly income rather than a single lump of cash.

This is a historical backtest, not a forecast. Past returns do not predict future results.

## Technical stack

- **Language:** Python 3.x
- **Data:** `yfinance` (adjusted close prices)
- **Manipulation:** `pandas`, `numpy`
- **Visualization:** `matplotlib`

## Portfolio under analysis

Growth-oriented core, balanced with quality and broader-market exposure.

| Ticker | Asset | Weight |
| :--- | :--- | :--- |
| SPYG | S&P 500 Growth ETF | 35% |
| BRK.B | Berkshire Hathaway (value / quality) | 25% |
| SMH | VanEck Semiconductor ETF | 16% |
| VTI | Vanguard Total Stock Market ETF | 14% |
| IEMG | iShares Core Emerging Markets ETF | 10% |
| **Total** | | **100%** |

## Simulation methodology

### 1. Data preparation

- Historical adjusted close prices from Yahoo Finance, **1 Jan 2020 – 26 Nov 2025**.
- Daily portfolio return = weighted average of the individual asset returns.

### 2. Scenario definitions

| Scenario | Initial investment | Monthly contribution | Horizon |
| :--- | :--- | :--- | :--- |
| A — Lump Sum | $5,000 on 1 Jan 2020 | $0 | ~5 years |
| B — DCA | $1,000 on 1 Jan 2020 | **$200** on the first trading day of each following month | ~5 years |

### 3. DCA calculation

Each trading day the script:

1. Applies the daily portfolio return to existing capital.
2. Adds the $200 contribution on the first trading day of each subsequent month.
3. Tracks capital contributed versus market value so the profit gap is visible.

## Getting started

```bash
pip install yfinance pandas numpy matplotlib
git clone https://github.com/Andalejo1109/Portfolio-management-and-optimization.git
cd Portfolio-management-and-optimization
python Simulacion_dca.py
```

The script prints the final metrics table and displays the comparative line chart.

## Author

Andrés Alejandro Rodríguez Lozano — economist, data scientist (MSc) and university professor. Investment decisions here are framed as statistical exercises, not market timing.

- GitHub Pages: [andalejo1109.github.io](https://andalejo1109.github.io/)
- LinkedIn: [linkedin.com/in/andalejo](https://www.linkedin.com/in/andalejo/)
- eToro profile: [@Andalejo1109](https://etoro.tw/4lkmjxn)

## License

MIT. Educational use. Not investment advice.
