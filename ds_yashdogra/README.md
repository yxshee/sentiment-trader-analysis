# Trader Performance & Market Sentiment Analysis

## 📊 Project Overview

This project analyzes the relationship between cryptocurrency trader behavior and Bitcoin market sentiment using data from the Hyperliquid trading platform and the Fear & Greed Index. The analysis reveals how market emotions influence trading outcomes, risk-taking behavior, and profitability patterns.

### 🎯 Objective
Explore how trading behavior (profitability, risk, volume, leverage) aligns with or diverges from overall market sentiment (fear vs greed) to identify trends and signals that could inform smarter trading strategies.

### 🔗 Google Colab Notebook
📓 **[Open in Google Colab](https://colab.research.google.com/drive/1IGRMeFVS5X_rmKHFThHw7MM8gvQyS8A9?usp=sharing)**


## 📊 Datasets

### 1. Hyperliquid Trading Data
- **Source**: Hyperliquid trading platform
- **Columns**: Account, Symbol, Execution Price, Size (Tokens & USD), Side, Timestamp, Closed PnL, Fee, Leverage
- **Coverage**: Trade-level records with complete transaction details
- **Format**: CSV with timestamps in IST
- **Download**: [Hyperliquid Trading Data CSV](https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view?usp=sharing)

### 2. Bitcoin Fear & Greed Index
- **Source**: Crypto Fear & Greed Index
- **Columns**: Date, Classification
- **Categories**: Extreme Fear, Fear, Neutral, Greed, Extreme Greed
- **Format**: Daily sentiment classifications
- **Download**: [Fear & Greed Index CSV](https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc-mnrYv__nhSf/view?usp=sharing)

## 🔍 Analysis Components

### 1. Data Processing
- Timestamp standardization and data quality validation
- Feature engineering for temporal patterns
- Sentiment-trade data integration (95%+ coverage)

### 2. Statistical Analysis
- **Performance**: Average/Median PnL by sentiment class
- **Behavior**: Trade size, frequency, and fee analysis
- **Risk**: PnL volatility and distribution patterns

### 3. Visualizations
- Sentiment-based performance comparisons
- Hourly PnL patterns and timing analysis
- Risk distribution and correlation studies

## 📈 Results

Below are the key figures generated from the analysis. Each image is linked from the `outputs/` folder and includes a brief interpretation tip to make it easier to act on the insight.

### Figure 1 — Daily Sentiment Mix
![Daily Classification Counts](./outputs/Daily%20Classification%20Counts.png)<br><br>
<br> <br>: Class balance across the study window. Heavier “Fear” or “Greed” regimes affect both backtest comparability and statistical power; use these counts when weighting or normalizing performance across regimes.

### Figure 2 — Feature Correlation Matrix
![Feature Correlation Matrix](./outputs/Feature%20Correlation%20Matrix.png)<br><br>
<br> <br>: Pairwise correlations between engineered features. Note any high-correlation clusters (e.g., token size vs USD notionals) that can cause multicollinearity in models and overstate feature importance.

### Figure 3 — Hourly Avg Closed PnL by Sentiment
![Hourly Avg Closed PnL by Sentiment](./outputs/Hourly%20Avg%20Closed%20PnL%20by%20Sentiment.png)<br><br>
<br> <br>: Intraday PnL patterns segmented by sentiment class. Look for hour blocks where “Greed” outperforms baseline and periods where “Fear” drags PnL—useful for timing filters and session-based risk throttling.

### Figure 4 — PnL Distribution by Sentiment
![PnL Distribution by Sentiment](./outputs/PnL%20Distribution%20by%20Sentiment.png) <br><br>
<br> <br>: Per-trade PnL distribution and tail behavior by regime. Skew and kurtosis differences indicate varying downside risk; “Fear” often shows fatter left tails—tighten stops or reduce size accordingly.

### Figure 5 — PnL vs Trade Size by Sentiment
![PnL vs Trade Size by Sentiment](./outputs/PnL%20vs%20Trade%20Size%20by%20Sentiment.png)<br><br>
<br> <br>: Relationship between position size and realized PnL. Watch for variance expansion with larger sizes and any non-linear payoffs; consider cap/scale rules that are regime-aware.

### Figure 6 — Symbols by Total PnL
![Symbols by Total PnL](./outputs/Symbols%20by%20Total%20PnL.png)<br><br>
<br> <br>: Concentration of profitability across symbols. Use this to guide symbol selection, risk budgets, and to check whether results depend on a few outliers versus broad-based performance.

## 🎯 Key Findings

### Performance by Market Sentiment
- **Fear Periods**: Distinct risk characteristics and trading volumes
- **Greed Periods**: Momentum patterns and increased position sizing
- **Neutral Markets**: Baseline performance benchmarks

### Intraday Patterns
- Identified optimal trading hours with higher profitability
- Revealed sentiment-specific time-of-day effects
- Highlighted liquidity variations across market emotions

### Risk-Return Insights
- Quantified PnL variations across sentiment classes
- Analyzed position sizing effects on profitability
- Identified fee efficiency patterns by sentiment

## 🚀 Strategic Implications

### 1. Sentiment-Adaptive Strategies
- **Fear**: Reduce exposure, emphasize risk management
- **Greed**: Scale positions with momentum, use trailing stops
- **Neutral**: Maintain baseline allocation approaches

### 2. Timing Optimization
- Focus trading during historically profitable hours
- Avoid low-liquidity periods with negative returns
# Trader Performance & Market Sentiment Analysis

Data-driven insights into how Bitcoin market sentiment shapes trader performance, behavior, and risk on Hyperliquid.

Author: Yash Dogra • Date: August 2025

## 🧭 Table of Contents
- Overview
- Objectives
- Data
- Methods
- Results & Charts
- Key Findings
- Practical Implications
- Reproducibility
- Limitations
- Next Steps
- Disclaimer

## 📊 Overview

This study examines the relationship between cryptocurrency trading outcomes and the Bitcoin Fear & Greed Index. We quantify how market emotion regimes (fear ↔ greed) relate to profitability, sizing behavior, timing patterns, and risk.

### 🎯 Objectives
- Measure performance differences across sentiment regimes
- Characterize behavior (size, frequency, leverage/fees) by regime
- Identify intraday timing patterns conditioned on sentiment
- Provide practical guardrails for sentiment-aware execution

### 🔗 Notebook
📓 Open in Google Colab: https://colab.research.google.com/drive/1IGRMeFVS5X_rmKHFThHw7MM8gvQyS8A9?usp=sharing

## 🧾 Data

1) Hyperliquid Trade History
- Source: Hyperliquid (account-level trade records)
- Columns (typical): account, symbol, exec price, size (tokens & USD), side, timestamp, closed PnL, fee, leverage
- Timezone: IST timestamps
- Repo copy: ./csv_files/historical_data.csv
- Optional external copy: https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view?usp=sharing

2) Bitcoin Fear & Greed Index
- Source: Alternative.me Crypto Fear & Greed Index
- Fields: date, classification ∈ {Extreme Fear, Fear, Neutral, Greed, Extreme Greed}
- Frequency: daily
- Repo copy: ./csv_files/fear_greed_index.csv
- Optional external copy: https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc-mnrYv__nhSf/view?usp=sharing

## 🧪 Methods

- Data processing: timestamp standardization, quality checks, and feature engineering for time-of-day patterns
- Sentiment join: map trades to same-day sentiment classification (high coverage; most trades map cleanly)
- Statistics: central tendency (mean/median), dispersion, distributional diagnostics by regime
- Visualization: comparative charts by regime, intraday panels, correlation heatmaps

## 🔎 Key Findings

- Performance differs by sentiment regime; fear/greed shifts are associated with changes in dispersion and tails
- Intraday seasonality exists and varies by regime; some hours show meaningfully different average outcomes
- Position sizing interacts with risk non-linearly; larger notional sizes can increase variance more than mean PnL
- Cross-feature correlations suggest careful feature selection or regularization in modeling workflows

## 🧭 Practical Implications

- Sentiment-adaptive risk: scale exposure down in Fear regimes; permit measured scaling in Greed, with trailing protection
- Timing filters: emphasize hours that historically align with positive expectancy under the active regime
- Sizing rules: regime-aware caps and step-ups to mitigate variance blow-ups at larger sizes
- Universe selection: lean into symbols with persistent contribution to PnL; monitor concentration risk

## 🔁 Reproducibility

- Notebook: run `notebook.ipynb` (Colab link above or locally)
- Data: by default, use the repo CSVs in `./csv_files/`; the notebook may include an optional cell to fetch from Google Drive if files are missing
- Environment (typical):
	- pandas>=1.3.0, matplotlib>=3.3.0, numpy>=1.20.0, gdown>=4.0.0

## ⚠️ Limitations

- Daily sentiment granularity may not capture intraday sentiment shifts
- Mapping trades to daily classes assumes same-day alignment; cross-day trades are treated by close time
- Sample composition and symbol mix can influence results; beware survivorship and selection biases
- Fees, slippage, and funding effects may vary across regimes and accounts

## 🚀 Next Steps

- Backtest sentiment-aware rules with walk-forward validation
- Add robust uncertainty bands and hypothesis tests to key charts
- Explore ML models for regime detection and transition probabilities
- Expand to multi-asset, multi-venue datasets for generalization

---

## 📌 Disclaimer
This analysis is for educational and research purposes only and is not financial advice. Past performance does not guarantee future results. Always validate before deploying capital.
