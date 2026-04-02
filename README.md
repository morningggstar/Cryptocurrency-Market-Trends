# Crypto Market Performance Dashboard — Power BI

An interactive Power BI dashboard tracking market cap, volume, and price trends across 7 major cryptocurrencies from 2017–2021. Built to demonstrate end-to-end business intelligence skills — from raw data ingestion to decision-ready visual reporting.

---

## Dashboard Preview

| Page | Screenshot |
|---|---|
| Market Overview | ![Dashboard Snapshot](screenshots/Dashboard_Snapshot.png) |
| Price Trends Analysis | ![Price Trends](screenshots/Price_Trends_Analysis.png) |

---

## Dashboard Overview

| Page | Description |
|---|---|
| Market Overview | KPI cards for volume, market cap, high/low/average prices with market cap time-series by date |
| Price Trends Analysis | High/low and open/close price trends by date with coin and year slicers |

---

## Key Features

- **Coin slicer** — Filter across BTC, ETH, BNB, XRP, Dogecoin, Stellar, NEM
- **Year slicer** — Drill into 2017, 2018, 2019, 2020, or 2021
- **KPI cards** — Volume, Market Cap, High, Low, Average price at a glance
- **Drill-through navigation** — Arrow buttons to switch between dashboard pages
- **Time-series visuals** — Market cap, open/close, and high/low trends over time

---

## Data Source

| Field | Details |
|---|---|
| Coins covered | BTC, ETH, BNB, XRP, Dogecoin, Stellar, NEM |
| Time range | 2017 – 2021 |
| Fields | SNo, Name, Symbol, Date, High, Low, Open, Close, Volume, MarketCap |
| Format | CSV per coin + consolidated Excel (CryptoData.xlsx) |
| Refresh | Manual |

---

## Tech Stack

- **Power BI Desktop** — Report development and data modeling
- **Power Query** — Data ingestion, cleaning, and transformation
- **DAX** — KPI measures and calculated columns
- **Excel / CSV** — Raw dataset storage

---

## How to Use

1. Clone or download this repository
2. Open `CryptoCurrency_Dashboard.pbix` in **Power BI Desktop**
3. Update the data source path in **Transform Data > Data Source Settings** to point to the `/dataset` folder
4. Refresh the dataset
5. Use the coin and year slicers to explore, and the arrow buttons to navigate between pages

---

## Project Structure

```
📁 Crypto-Market-Performance-Dashboard/
├── 📊 CryptoCurrency_Dashboard.pbix
├── 📁 dataset/
│   ├── CryptoData.xlsx
│   ├── coin_Bitcoin.csv
│   ├── coin_Ethereum.csv
│   ├── coin_BinanceCoin.csv
│   ├── coin_XRP.csv
│   ├── coin_Dogecoin.csv
│   ├── coin_Stellar.csv
│   └── coin_NEM.csv
├── 📁 screenshots/
│   ├── Dashboard_Snapshot.png
│   └── Price_Trends_Analysis.png
└── 📄 README.md
```

---

## Skills Demonstrated

`Power BI` `DAX` `Power Query` `Data Modeling` `Business Intelligence` `Data Visualization` `KPI Reporting` `ETL`

---

## About

Built as part of a portfolio to demonstrate Power BI and data analytics skills. This project reflects real-world BI workflows — raw data → cleaned model → actionable dashboard — aligned with enterprise reporting standards.


