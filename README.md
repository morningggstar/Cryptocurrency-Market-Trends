# Cryptocurrency Market Trends — Power BI Dashboard

An interactive Power BI dashboard analyzing cryptocurrency market behavior, price trends, volume patterns, and volatility indicators across major coins. Built to demonstrate end-to-end business intelligence skills — from raw data ingestion to decision-ready visual reporting.

---

## Dashboard Overview

| Page | Description |
|---|---|
| Market Overview | High-level KPIs — market cap, dominance, 24h change across top coins |
| Price Trends | Time-series analysis of historical price movements with moving averages |
| Volume Analysis | Trading volume patterns and correlation with price action |
| Volatility Metrics | Risk indicators and % change distributions |

> **Screenshots** are available in the `/screenshots` folder.

---

## Key Features

- **Dynamic filtering** — Slice by coin, date range, and market cap tier
- **DAX measures** — Custom calculations for % change, rolling averages, and volatility scores
- **Data modeling** — Star schema with a central fact table and supporting dimension tables
- **Drill-through pages** — Click any coin to deep-dive into its individual metrics
- **Bookmarks & buttons** — Navigation between report pages without using Power BI tabs

---

## Data Source

| Field | Details |
|---|---|
| Source | [CoinGecko API](https://www.coingecko.com/en/api) / CSV export |
| Coins covered | BTC, ETH, BNB, SOL, XRP *(update as applicable)* |
| Time range | Jan 2023 – Present |
| Refresh | Manual / Scheduled *(update as applicable)* |

---

## Tech Stack

- **Power BI Desktop** — Report development and data modeling
- **Power Query (M)** — Data ingestion, cleaning, and transformation
- **DAX** — Measures and calculated columns
- **Excel / CSV** — Raw dataset storage

---

## DAX Highlights

```dax
-- 7-Day Rolling Average Price
Rolling Avg Price =
AVERAGEX(
    DATESINPERIOD('Date'[Date], LASTDATE('Date'[Date]), -7, DAY),
    [Average Close Price]
)

-- % Change from Previous Period
Price Change % =
DIVIDE(
    [Latest Close Price] - [Previous Close Price],
    [Previous Close Price],
    0
)
```

---

## Data Model

```
FactPrices (date, coin_id, open, high, low, close, volume, market_cap)
    |
    |--- DimCoin (coin_id, name, symbol, category)
    |--- DimDate (date, year, month, quarter, week)
```

---

## How to Use

1. Clone or download this repository
2. Open `Cryptocurrency_Market_Trends.pbix` in **Power BI Desktop**
3. If using live data, update the data source path in **Transform Data > Data Source Settings**
4. Refresh the dataset
5. Explore the report using the navigation buttons on each page

---

## Project Structure

```
📁 Cryptocurrency-Market-Trends/
├── 📊 Cryptocurrency_Market_Trends.pbix
├── 📁 dataset/
│   └── crypto_prices.csv
├── 📁 screenshots/
│   ├── overview.png
│   ├── price_trends.png
│   └── volume_analysis.png
└── 📄 README.md
```

---

## Skills Demonstrated

`Power BI` `DAX` `Data Modeling` `Power Query` `Business Intelligence` `Data Visualization` `KPI Reporting` `ETL`

---




