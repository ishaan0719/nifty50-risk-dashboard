# NIFTY 50 Portfolio Risk Dashboard

An interactive portfolio risk dashboard built in Python analyzing all 50 constituents of the NIFTY 50 index. The dashboard provides a snapshot of key risk and return metrics derived from a single-day market data snapshot.

## Dashboard Preview

> Open `nifty50_dashboard.html` in any browser for the full interactive experience.

## Features

- **365-Day Return Analysis** — visual comparison of annual returns across all 50 stocks, color coded green/red
- **Drawdown from 52-Week High** — identifies how far each stock has fallen from its yearly peak
- **Portfolio Weight Distribution** — pie chart of the top 15 holdings by traded value
- **Risk vs Return Scatter** — bubble chart plotting each stock's risk score against its 1-year return, with bubble size representing portfolio weight

## Metrics Computed

| Metric | Description |
|---|---|
| Drawdown % | How far LTP has fallen from 52W high |
| Recovery % | How much LTP has recovered from 52W low |
| Range Position | Where LTP sits in the 52W range (0 = at low, 1 = at high) |
| Portfolio Weight | Stock's share of total traded value |
| Risk Score | Composite score combining range position and return volatility |

## Project Structure

nifty50-risk-dashboard/
├── nifty50_dashboard.html    # Standalone interactive dashboard
├── Nifty50Data - Sheet1.csv  # Raw market snapshot data (NSE)
├── notebook.ipynb            # Full analysis notebook
└── README.md
## How to Run

1. Clone the repo
2. Open `notebook.ipynb` in JupyterHub or Jupyter Notebook
3. Run all cells in order
4. Dashboard renders inline or saves as `nifty50_dashboard.html`

## Data Source

Single-day snapshot of NIFTY 50 constituents downloaded from the [NSE India](https://www.nseindia.com) website. Data includes LTP, 52-week high/low, 30-day and 365-day percentage change, and traded volume/value.

## Tech Stack

- Python 3.9
- pandas — data cleaning and manipulation
- numpy — metric calculations
- plotly — interactive visualizations

## Limitations & Next Steps

This dashboard currently uses a single-day snapshot. Future improvements planned:

- [ ] Integrate historical price CSVs for time-series metrics
- [ ] Add Value at Risk (VaR) using historical simulation
- [ ] Add Sharpe Ratio and Beta vs NIFTY 50 benchmark
- [ ] Add sector-wise grouping and color coding
- [ ] Build Streamlit version for live data updates

## Author

Ishaan Srivastava
Mechanical Engineering, IIT Bombay
