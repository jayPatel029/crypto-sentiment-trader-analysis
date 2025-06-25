# Crypto Trade-Sentiment Analysis Project

## 📌 Overview

This project explores the relationship between market sentiment and trading behavior using historical trading data and Fear & Greed Index sentiment scores. It combines data cleaning, merging, exploratory analysis, and pattern recognition — ultimately drawing insights into trader profitability and risk appetite across sentiment phases.

Ideal for showcasing skills in **Python, pandas, data visualization, and statistical analysis** for a data intern role.

---

## 📁 Dataset Summary

- `history.csv` – Raw trade history with fields like `closed_pnl`, `side`, `execution_price`, `size_usd`, etc.
- `fear_and_greed.csv` – Market sentiment data with `value` (0–100) and `classification` (e.g., "Fear", "Greed").
- `merged.csv` – Cleaned and merged dataset used for final analysis (generated during preprocessing).

---

## 📊 Project Workflow

### 🔹 Phase 1: Load & Inspect the Data

- Check shapes, columns, dtypes, and NaNs
- Print value counts and preview raw data

> 📄 Check: `Phase 1 – Data Loading & Initial Inspection`

---

### 🔹 Phase 2: Data Cleaning and Preparation

- Handle missing/corrupt data
- Drop redundant columns (e.g., duplicate `direction`)
- Create derived features:
  - `Trade Value per Token`
  - `Trade Day` from timestamp
  - Sanity checks for key numerical fields

> 📄 Check: `Phase 2 – Cleaning & Feature Engineering`

---

### 🔹 Phase 3: Merge Sentiment with Trade Data

- Merge on `timestamp_ist` and `date`
- Post-merge validation to ensure sentiment was joined correctly

> 📄 Check: `Phase 3 – Merging Sentiment & Trades`

---

### 🔹 Phase 4: Exploratory Data Analysis (EDA)

- Line plots for sentiment trends
- Trade volume & count per sentiment
- Avg & median PnL by classification
- Win rate analysis

> 📄 Check: `Phase 4 – EDA & Visual Trends`

---

### 🔹 Phase 5: Pattern Detection & Insights

- Correlation matrix: `sentiment score` vs `PnL`, `size_usd`
- Trader segmentation: Top performers in Fear vs Greed
- Risk profiling: Avg trade size by sentiment

> 📄 Check: `Phase 5 – Statistical Relationships`

---

### 🔹 Phase 6: Visualization & Reporting

- Box plots, heatmaps, and bar charts
- Summary tables: win rate, avg PnL, top traders
- Final insights as markdown summary

> 📄 Check: `Phase 6 – Insights & Reporting`

---

## 📈 Key Insights Summary

👉 Full Insights Report

- **Extreme Greed yields highest avg PnL**, but **Fear traders also perform strongly**.
- Some traders consistently profit in **low-sentiment periods**, showing contrarian behavior.
- **Win rate is not sentiment-driven**; big wins matter more than frequent wins.
- **Trade size and fees are highly correlated**, hinting at platform monetization structure.

---

## 💡 Ideas for Extension

- 📊 Build a Streamlit dashboard for interactive insights
- 🔍 Add volatility or token price tracking
- 🧠 Use ML to predict PnL based on sentiment & trade features
