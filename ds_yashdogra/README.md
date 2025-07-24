# Trader Performance & Market Sentiment Analysis

## 📊 Project Overview

This project analyzes the relationship between cryptocurrency trader behavior and Bitcoin market sentiment using data from Hyperliquid trading platform and the Fear & Greed Index. The analysis reveals how market emotions influence trading outcomes, risk-taking behavior, and profitability patterns.

### 🎯 Objective
Explore how trading behavior (profitability, risk, volume, leverage) aligns or diverges from overall market sentiment (fear vs greed) to identify hidden trends and signals that could influence smarter trading strategies.

### 🔗 Google Colab Notebook
📓 **[Open in Google Colab](https://colab.research.google.com/drive/1IGRMeFVS5X_rmKHFThHw7MM8gvQyS8A9?usp=sharing)**

## 📂 Project Structure

```
ds_yashdogra/
├── notebook.ipynb                    # Main analysis notebook (Jupyter/Colab)
├── csv_files/                        # Data storage
│   ├── historical_data.csv          # Hyperliquid trading records
│   └── fear_greed_index.csv         # Bitcoin Fear & Greed Index data
├── outputs/                          # Generated visualizations
│   ├── 01_avg_pnl_by_sentiment.png     # Average PnL across sentiment classes
│   ├── 02_avg_trade_size_by_sentiment.png # Trade size patterns by sentiment
│   ├── 03_avg_fee_by_sentiment.png     # Fee analysis by sentiment
│   ├── 04_trade_count_by_sentiment.png # Trading activity levels
│   ├── 05_hourly_pnl_by_sentiment.png  # Intraday performance patterns
│   └── 06_pnl_distribution_boxplot.png # PnL distribution analysis
└── README.md                         # This file
```

## 📊 Datasets

### 1. Historical Trader Data (Hyperliquid)
- **Source**: Hyperliquid trading platform
- **Columns**: Account, Symbol, Execution Price, Size (Tokens & USD), Side, Timestamp, Closed PnL, Fee, Leverage
- **Coverage**: Trade-level records with complete transaction details
- **Format**: CSV with timestamp in IST format

### 2. Bitcoin Market Sentiment (Fear & Greed Index)
- **Source**: Crypto Fear & Greed Index
- **Columns**: Date, Classification (Fear/Greed levels)
- **Categories**: Extreme Fear, Fear, Neutral, Greed, Extreme Greed
- **Format**: Daily sentiment classifications

## 🔍 Key Analysis Components

### 1. Data Preprocessing & Harmonization
- ✅ Timestamp parsing and date standardization
- ✅ Data quality checks and missing value handling
- ✅ Feature engineering (hourly patterns, date extraction)
- ✅ Sentiment-trade data merger with 95%+ coverage

### 2. Statistical Analysis by Sentiment
- **Performance Metrics**: Average PnL, Median PnL, Total PnL
- **Behavioral Metrics**: Trade size, frequency, fee analysis
- **Risk Assessment**: PnL volatility and distribution analysis

### 3. Visual Explorations
- **Sentiment Performance**: Bar charts comparing key metrics across sentiment classes
- **Temporal Patterns**: Hourly PnL analysis revealing intraday effects
- **Risk Distribution**: Boxplot analysis of PnL variability
- **Asset Analysis**: Top-performing symbols identification
- **Correlation Studies**: Feature relationship mapping

## 🎯 Key Insights & Findings

### 💡 Sentiment-Driven Performance Patterns
- **Fear Periods**: Show different risk characteristics and trading volumes
- **Greed Periods**: Display distinct momentum patterns and position sizing
- **Neutral Markets**: Provide baseline performance benchmarks

### ⏰ Intraday Trading Patterns
- Identified optimal trading hours with consistently higher PnL
- Revealed sentiment-specific time-of-day effects
- Highlighted liquidity patterns across different market emotions

### 📈 Risk-Return Relationships
- Quantified PnL distribution variations across sentiment classes
- Identified outlier patterns and tail risk characteristics
- Analyzed correlation between trade size and profitability

### 🎮 Behavioral Insights
- **Position Sizing**: How sentiment affects risk appetite
- **Trading Frequency**: Activity patterns during different market phases
- **Fee Impact**: Cost efficiency across sentiment regimes

## 🚀 Strategic Recommendations

### 1. Sentiment-Adaptive Position Sizing
- **Fear Markets**: Reduce exposure, focus on risk management
- **Greed Markets**: Scale into winners with trailing stops
- **Neutral Markets**: Maintain baseline allocation strategies

### 2. Optimal Timing Strategies
- **Intraday Focus**: Concentrate trading during historically profitable hours
- **Avoid Low-Liquidity**: Skip periods with negative expectancy
- **Sentiment Transitions**: Monitor regime changes for repositioning

### 3. Risk Management Framework
- **Dynamic Stops**: Tighter controls during Fear, wider during Greed momentum
- **Volatility Adjustment**: Sentiment-specific position sizing rules
- **Correlation Awareness**: Account for cross-asset sentiment effects

### 4. Asset Selection Criteria
- **Symbol Rotation**: Prioritize consistently profitable assets per regime
- **Momentum Identification**: Focus on top performers during Greed phases
- **Defensive Selection**: Quality assets during Fear periods

## 🛠️ Technical Implementation

### Requirements
```
pandas>=1.3.0
matplotlib>=3.3.0
numpy>=1.20.0
gdown>=4.0.0
```

### Running the Analysis
1. **Google Colab** (Recommended): [Open notebook directly](https://colab.research.google.com/drive/1IGRMeFVS5X_rmKHFThHw7MM8gvQyS8A9?usp=sharing)
2. **Local Jupyter**: `jupyter notebook notebook.ipynb`
3. **VS Code**: Open `notebook.ipynb` in VS Code with Jupyter extension

### Data Loading
The notebook includes automatic data download from Google Drive:
- Historical trading data: `1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs`
- Fear & Greed Index: `1PgQC0tO8XN-wqkNyghWc_-mnrYv_nhSf`

## 📊 Output Visualizations

| Visualization | Description | Key Insights |
|--------------|-------------|--------------|
| `01_avg_pnl_by_sentiment.png` | Average PnL across sentiment classes | Performance comparison by market emotion |
| `02_avg_trade_size_by_sentiment.png` | Trade size patterns by sentiment | Risk appetite variations |
| `03_avg_fee_by_sentiment.png` | Fee analysis by sentiment | Cost efficiency patterns |
| `04_trade_count_by_sentiment.png` | Trading activity levels | Behavioral frequency analysis |
| `05_hourly_pnl_by_sentiment.png` | Intraday performance patterns | Optimal timing identification |
| `06_pnl_distribution_boxplot.png` | PnL distribution analysis | Risk and outlier assessment |

## 🔬 Methodology

### Data Quality Assurance
- ✅ Comprehensive data validation and cleaning
- ✅ Timestamp consistency checks across datasets
- ✅ Missing value analysis and handling strategies
- ✅ Outlier detection and treatment protocols

### Statistical Rigor
- **Correlation Analysis**: Pearson coefficients with significance testing
- **Distribution Analysis**: Comprehensive statistical summaries
- **Temporal Analysis**: Time-series aware pattern recognition
- **Robustness Checks**: Multiple metrics (mean, median) for validation

### Visualization Standards
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
