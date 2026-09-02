# Real-Time Bitcoin Sentiment Analysis Using txtai

This project evaluates whether real-time news sentiment can act as a leading indicator for short-term Bitcoin price movements. It combines semantic sentiment analysis with historical price data and a time-series forecasting model.

## Tools & Data Sources

- [**txtai**](https://github.com/neuml/txtai) — semantic search and sentiment scoring on news headlines
- [**NewsAPI**](https://newsapi.org/) — real-time Bitcoin-related news headlines
- [**CoinGecko API**](https://www.coingecko.com/en/api) — historical Bitcoin price data
- **ARIMA** (statsmodels) — time-series forecasting
- **pandas / matplotlib / seaborn** — data processing and visualization

## Pipeline

1. **Fetch news & score sentiment** — Pull live Bitcoin-related headlines via NewsAPI and score each headline's sentiment using txtai's semantic pipeline.
2. **Fetch price data** — Retrieve historical Bitcoin prices (USD) from CoinGecko.
3. **Merge & align** — Join sentiment and price data on date to build a unified time series.
4. **Clean & validate** — Handle duplicate dates (grouped average), resample to daily frequency, forward-fill missing values, and run sanity checks (NaN counts, min/max price bounds) before modeling.
5. **Visualize** — Plot Bitcoin price trends and a stacked bar chart of daily sentiment distribution.
6. **Forecast** — Fit an ARIMA(5,1,2) model on 30 days of price history to forecast the next 7 days.

## Key Finding

Negative news sentiment consistently preceded short-term Bitcoin price drops, suggesting sentiment can act as an early-warning signal rather than simply tracking price after the fact.

## Setup

This notebook reads the NewsAPI key from an environment variable rather than hardcoding it:

```bash
export NEWS_API_KEY="your_newsapi_key_here"
```

Then run the notebook (`txtai_API.ipynb`) top to bottom. `txtai_utils.py` contains the helper functions (`fetch_bitcoin_headlines`, `analyze_sentiment`, `run_arima_forecast`) imported by the notebook.

## Files

| File | Description |
|---|---|
| `txtai_API.ipynb` | Main notebook — full pipeline from data fetch to forecast |
| `txtai_utils.py` | Helper functions for headline fetching, sentiment scoring, and ARIMA forecasting |

## Possible Extensions

- Backtest whether acting on the sentiment signal would have improved returns vs. a buy-and-hold baseline
- Expand beyond Bitcoin to other major cryptocurrencies for comparison
- Replace ARIMA with a model that can incorporate sentiment as an exogenous variable (e.g., ARIMAX)
