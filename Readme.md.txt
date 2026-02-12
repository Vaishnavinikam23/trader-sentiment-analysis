Trader Performance vs Market Sentiment Analysis
Objective

This project analyzes how Bitcoin market sentiment (Fear vs Greed) influences trader behavior and performance on Hyperliquid.
The goal is to identify regime-dependent patterns and derive actionable trading strategy rules based on empirical data.

Dataset

Two datasets were used:

Bitcoin Market Sentiment

Daily Fear / Greed classification

Hyperliquid Historical Trader Data

Account activity

Trade direction

Trade size

Profit & Loss (PnL)

Timestamp

Methodology
1. Data Preparation

Converted timestamps to daily level

Merged trading data with daily sentiment

Removed unmatched dates

Aggregated metrics per trader per day

2. Feature Engineering

Key metrics created:

Daily PnL

Win rate

Loss frequency (drawdown proxy)

Trade frequency

Average position size

Long/Short ratio

Trader consistency score

3. Segmentation

Traders were categorized into:

Frequent vs Infrequent traders

Consistent vs Inconsistent traders

Key Findings
Performance vs Sentiment

Win rate remains nearly constant across regimes (~36%)

Fear periods show higher downside volatility

Median performance is stronger during Greed regimes

Behavioral Changes

Traders exhibit stronger long bias during Fear (bottom-picking behavior)

Activity level impacts resilience to volatility

Segment Differences

Frequent and consistent traders perform more robustly across regimes

Inconsistent traders underperform significantly during Fear periods

Strategy Recommendations

1. Regime-Based Trader Allocation
During Fear regimes, allocate capital preferentially to historically consistent and high-frequency traders while reducing exposure to infrequent participants.

2. Long-Exposure Control During Fear
Limit position size for long trades during Fear regimes to reduce volatility-driven drawdowns.

How to Run

Install dependencies:

pip install pandas numpy matplotlib seaborn


Open and run:

Trader_Sentiment_Analysis.ipynb


Run all cells sequentially.

Project Structure
Trader_Sentiment_Analysis/
│
├── Trader_Sentiment_Analysis.ipynb
├── README.md

Conclusion

Market sentiment does not significantly change trading accuracy but strongly affects risk distribution and trader behavior.
Filtering trader participation and controlling exposure based on sentiment regime improves risk-adjusted performance.