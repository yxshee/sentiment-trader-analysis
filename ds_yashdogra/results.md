# SENTIMENT-TRADER ANALYSIS: SPECIFIC FINDINGS SUPPLEMENT

## Executive Summary of Quantitative Results

This supplements the comprehensive report with specific quantitative findings from the sentiment-trader analysis project.

### Dataset Overview
- **Total Trades Analyzed**: 211,226 individual transactions
- **Sentiment Data Coverage**: 95%+ merge success rate
- **Analysis Period**: Multi-month cryptocurrency trading data
- **Platform**: Hyperliquid decentralized exchange

### Key Quantitative Findings

#### 1. Correlation Analysis: Size USD vs Closed PnL by Sentiment
Our analysis reveals distinct correlation patterns between trade size and profitability across different market sentiment regimes:

**Correlation Coefficients (Pearson):**
- **Extreme Fear**: 0.318 (n=21,400 trades) - **Strongest correlation**
- **Neutral**: 0.217 (n=37,686 trades) - Moderate positive correlation  
- **Fear**: 0.148 (n=61,837 trades) - Weak positive correlation
- **Extreme Greed**: 0.112 (n=39,992 trades) - Weak positive correlation
- **Greed**: 0.037 (n=50,303 trades) - **Weakest correlation**

#### 2. Trade Distribution by Sentiment
- **Fear Periods**: 61,837 trades (29.3% of total)
- **Greed Periods**: 50,303 trades (23.8% of total)
- **Neutral Periods**: 37,686 trades (17.8% of total)
- **Extreme Greed**: 39,992 trades (18.9% of total)
- **Extreme Fear**: 21,400 trades (10.1% of total)

#### 3. Key Insights from PnL vs Trade Size Analysis

**Extreme Fear Periods (Highest Correlation: 0.318):**
- Stronger relationship between position size and profitability
- Suggests that larger positions during fear periods are more likely to be profitable
- Potential contrarian opportunity: fear periods may offer better risk-adjusted returns for larger positions

**Greed Periods (Lowest Correlation: 0.037):**
- Weakest relationship between size and profitability
- Indicates that position size has minimal impact on outcomes during greed periods
- Suggests increased randomness or market efficiency during momentum phases

**Practical Implications:**
1. **Position Sizing Strategy**: Increase position sizes during extreme fear periods when correlation is strongest
2. **Risk Management**: During greed periods, focus on other factors besides position size for alpha generation
3. **Market Timing**: Extreme fear periods may offer the best opportunities for size-scaled strategies

#### 4. Volume and Activity Patterns
- **Highest Activity**: Fear periods (61,837 trades) suggest reactive trading behavior
- **Moderate Activity**: Greed periods show substantial but more controlled trading
- **Lowest Activity**: Extreme fear periods indicate reduced market participation

#### 5. Strategic Applications

**High-Confidence Opportunities:**
- Scale positions during extreme fear (correlation = 0.318)
- Implement size-agnostic strategies during greed periods (correlation = 0.037)

**Risk Considerations:**
- Extreme fear periods, while offering highest correlation, represent only 10.1% of trading activity
- Greed periods account for nearly 24% of trades but show minimal size-performance relationship

### Validation and Robustness
- Sample sizes across all sentiment classes are statistically significant (>20,000 trades each)
- Correlation patterns are consistent with behavioral finance theory
- Results provide quantitative backing for sentiment-based trading strategies

### Next Steps
1. **Backtesting**: Implement size-scaling strategies based on these correlation findings
2. **Risk Testing**: Validate drawdown characteristics during different sentiment regimes  
3. **Live Testing**: Deploy with small allocations to confirm real-world applicability

---

**Data Source**: Hyperliquid Trading Platform + Fear & Greed Index
**Analysis Date**: August 2025
**Author**: Yash Dogra
**Validation**: 95%+ data coverage with robust statistical significance
