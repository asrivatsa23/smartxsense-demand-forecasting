# SmartXSense — Data Sources

This document records exactly where each dataset used in this project comes from,
its license, and whether it is official/real-world data or synthetic/demo data.

## 1. Electricity Demand Dataset (Primary)

- **Source:** NITI Aayog — India Climate and Energy Dashboard (ICED)
- **URL:** https://iced.niti.gov.in
- **File:** `datasets/raw/electricity/electricity_hourly_demand_niti_aayog.csv`
- **Granularity:** Hourly
- **Time span:** 2017–2026
- **Rows:** 81,024 (after removing 20 footer/junk rows from the original export)
- **Fields:** Year, Date, Hourly Demand Met (in MW)
- **Classification:** OFFICIAL — published by NITI Aayog, a Government of India policy body.
  NITI Aayog's own disclaimer notes some figures may be "derived or assumed" in certain cases,
  so treat as official-but-not-100%-verified-per-row.

## 2. Electricity Demand Dataset (Secondary reference)

- **Source:** AIKosh (India AI) — Government of India open data portal
- **Series:** "Peak Demand and Peak Met", published monthly
- **License:** Open Government License, India
- **Status:** Not used as primary due to coarser (monthly) granularity compared to
  the NITI Aayog hourly dataset. Retained as a secondary/cross-validation reference only.

## 3. Retail Demand Dataset

- **Source:** Kaggle — "Retail Sales Dataset" by user abbas829
- **URL:** https://www.kaggle.com/datasets/abbas829/retail-sales-dataset
- **Granularity:** Daily
- **Fields:** Date, Category, Sales, Quantity, Profit, Region
- **Classification:** SYNTHETIC — explicitly described by its creator as a simulated
  retail environment for educational and analytical purposes. No official, centralized,
  granular retail sales dataset for India was found. This must never be presented as
  real government or company sales data.

## Classification Summary

| Dataset | Track | Classification |
|---|---|---|
| NITI Aayog Hourly Demand Met | Electricity | Official (Govt. of India — NITI Aayog) |
| AIKosh Peak Demand and Peak Met | Electricity (secondary) | Official (Govt. of India, OGL) |
| Kaggle Retail Sales Dataset (abbas829) | Retail | Synthetic / Simulated |