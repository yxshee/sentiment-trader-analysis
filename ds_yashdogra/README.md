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

### 2. Bitcoin Fear & Greed Index
- **Source**: Crypto Fear & Greed Index
- **Columns**: Date, Classification
- **Categories**: Extreme Fear, Fear, Neutral, Greed, Extreme Greed
- **Format**: Daily sentiment classifications

## 🔗 Dataset Links

1. Historical Trader Data:
   [Google Drive Link](https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view?usp=sharing)

2. Fear & Greed Index:
   [Google Drive Link](https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc_-mnrYv_nhSf/view?usp=sharing)

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
- Monitor sentiment transitions for repositioning

### 3. Risk Management
- Implement sentiment-specific position sizing
- Adjust stops based on market emotion regime
- Account for volatility differences across sentiment classes

## 🛠️ Technical Setup

### Requirements
```
pandas>=1.3.0
matplotlib>=3.3.0
numpy>=1.20.0
gdown>=4.0.0
```

### Usage
1. **Google Colab** (Recommended): [Open notebook](https://colab.research.google.com/drive/1IGRMeFVS5X_rmKHFThHw7MM8gvQyS8A9?usp=sharing)
2. **Local**: `notebook.ipynb`

Data is automatically downloaded from Google Drive within the notebook.



## 🔬 Methodology

### Data Quality
- Comprehensive validation and cleaning protocols
- Timestamp consistency across datasets
- Statistical outlier detection and treatment

### Analysis Approach
- Correlation analysis with significance testing
- Multiple validation metrics (mean, median)
- Time-series pattern recognition
- Publication-ready visualizations

## 🎯 Future Directions

### Validation & Implementation
- Backtesting with sentiment-based rules
- Walk-forward validation to avoid look-ahead bias
- Paper trading for live strategy validation

### Advanced Analytics
- Machine learning for sentiment prediction
- Multi-asset portfolio optimization
- Alternative sentiment data integration

---

**Disclaimer**: This analysis is for educational and research purposes. Past performance does not guarantee future results.

**Author**: Yash Dogra  
**Date**: August 2025  
**Project**: Web3 Trading Team Data Science Analysis
- Clear, publication-ready charts with proper labeling
- Consistent color schemes and formatting
- Interactive elements where applicable
- Statistical annotations and confidence indicators

## 🎯 Next Steps & Extensions

### Validation Framework
1. **Backtesting**: Implement strategy rules by sentiment regime
2. **Walk-Forward Validation**: Avoid look-ahead bias in testing
3. **Paper Trading**: Live validation with small allocation
4. **Performance Monitoring**: Real-time strategy tracking

### Advanced Analytics
- **Machine Learning**: Predictive models for sentiment transitions
- **Portfolio Optimization**: Multi-asset sentiment-aware allocation
- **Risk Models**: Advanced VaR calculations by sentiment
- **Alternative Data**: Integration of additional sentiment sources

### Operational Integration
- **Alert Systems**: Sentiment regime change notifications
- **Automated Execution**: Rule-based trading implementation
- **Risk Controls**: Dynamic position sizing automation
- **Performance Attribution**: Sentiment-based P&L decomposition

## 📝 Research Notes

This analysis forms part of a comprehensive trading strategy research project. The findings provide empirical evidence for sentiment-driven trading approaches and offer quantitative backing for intuitive market observations.

### Academic Relevance
- Behavioral finance applications in cryptocurrency markets
- Sentiment analysis integration in quantitative trading
- Risk management optimization through market psychology

### Industry Applications
- Hedge fund strategy development
- Proprietary trading desk optimization
- Risk management framework enhancement
- Systematic trading strategy validation

---

**Disclaimer**: This analysis is for educational and research purposes. Past performance does not guarantee future results. Always conduct thorough testing before implementing any trading strategy.

**Author**: Yash Dogra  
**Date**: August 2025  
**Assignment**: Web3 Trading Team Data Science Analysis

# Data Science Assignment Instructions – Web3 Trading Team

## 📂 Standardized Submission Format

All candidate submissions must strictly follow this structure. Non-compliance will result in rejection of the application.

```
ds_yashdogra/
├── notebook.ipynb  # All work done in Google Colab
├── notebook_2.ipynb  # (Optional) Additional Colab notebook if needed
├── csv_files/       # Store all CSVs or data outputs here
│   └── *.csv        # Intermediate or processed data files
├── outputs/         # Store all visual outputs, graphs, or charts here
│   └── *.png/*.jpg  # Image results of EDA, charts, etc.
├── ds_report.pdf    # Final summarized insights and explanations
└── README.md        # (Optional but encouraged) Setup instructions, notes
```

- All code must be shared as **Google Colab links** with access set to 'Anyone with the link can view'.
- The exact same structure must be updated in the GitHub repository as well.
- Failing to comply with any of the above instructions will result in immediate rejection.

## 📂 Assignment Overview

You are expected to explore and analyze the relationship between trader behavior and market sentiment using two key datasets.

## 📂 Datasets

1. **Bitcoin Market Sentiment Dataset**
   - Columns: `Date`, `Classification` (Fear / Greed)

2. **Historical Trader Data from Hyperliquid**
   - Columns include: `account`, `symbol`, `execution price`, `size`, `side`, `time`, `start position`, `event`, `closedPnL`, `leverage`, etc.

## 📂 Objective

Analyze how trading behavior (profitability, risk, volume, leverage) aligns or diverges from overall market sentiment (fear vs greed). Identify hidden trends or signals that could influence smarter trading strategies.

## 📂 Dataset Links

1. Historical Trader Data:
   https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view?usp=sharing

2. Fear & Greed Index:
   https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc_-mnrYv_nhSf/view?usp=sharing

## 📂 Apply Now!

This assignment is the first step in our hiring process. Top-performing candidates will be shortlisted for an interview.

Apply now and take the next step in your data science career with one of the most innovative teams in Web3 trading!
