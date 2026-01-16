**Cross-Asset Portfolio Optimization using Risk Parity**

Arbitrage Arena – IIT Madras (Prelims Submission)

**Overview**

This project was developed as part of Arbitrage Arena, a competitive analytics challenge conducted by IIT Madras. The objective was to design a robust, diversified portfolio across multiple asset classes while maintaining stable risk exposure across market regimes.

Instead of chasing returns through prediction-heavy models, this project focuses on risk-aware allocation, emphasizing stability, diversification, and interpretability.

**Problem Statement**

  Selected Problem: Cross-Asset Portfolio Optimization
  
  The goal was to construct a portfolio that:
  
  1. Spans equities, index instruments, and commodities
  
  2. Maximizes risk-adjusted returns
  
  3. Controls drawdowns during volatile periods
  
  4. Remains interpretable and robust across market conditions

**Assets & Data**

  The portfolio is built using daily historical OHLC price data over a period of approximately 11–12 years.

**Asset Classes**

  1. Equities: AAPL, MSFT, NVDA, AMZN, META, TSLA
  
  2. Index: NASDAQ
  
  3. Commodities: Gold, Silver, Crude Oil

**Approach & Methodology**
**1. Data Preprocessing**
  
  The initial phase ensures clean, aligned, and analysis-ready data:
  
  1. Timestamp standardization across all assets
  
  2. Numeric conversion of OHLC values
  
  3. Missing value handling using forward and backward filling
  
  4. Visual validation of price series using OHLC plots
  
  5. Computation of daily and log returns
  
  This step ensures that all assets operate on a consistent time axis, which is critical for portfolio construction.

**2. Exploratory Data Analysis (EDA)**

  1. EDA was performed to understand asset behavior and relationships:
  
  2. Long-term price trends and regime shifts
  
  3. Return distributions and volatility clustering
  
  4. Correlation analysis across asset classes
  
  5. Identification of diversification benefits

  This analysis guided the decision to adopt a risk parity approach rather than return forecasting.

**3. Feature Engineering**

  1. The model relies on risk-based features, not predictive signals:
  
  2. Rolling volatility as the primary risk metric
  
  3. Correlation matrices to assess diversification
  
  4. Identification of low-correlation assets for stability
  
  These features are designed to support volatility-aware allocation.

**4. Portfolio Construction – Risk Parity**

  1. The portfolio uses a Risk Parity framework, where allocation is based on equalizing risk contribution, not capital allocation.
  
  2. Key principles:
  
    a. No return prediction (reduces overfitting)
  
    b. Long-only positions
  
    c. Fully invested portfolio
  
    d. No leverage

  3. Weight formulation: wi​=∑j​(1/σj​)1/σi​​
  
  This ensures assets with lower volatility receive higher weights, balancing overall risk.

**5. Backtesting Framework**

  The strategy is evaluated using a daily backtest:
  
  1. Static risk parity weights
  
  2. Portfolio returns computed as weighted asset returns
  
  3. Portfolio value calculated via cumulative compounding
  
  4. Transaction costs assumed zero for baseline analysis

**6. Evaluation Metrics**

  1. Portfolio performance is assessed using:
  
  2. Annualized Return
  
  3. Annualized Volatility
  
  4. Sharpe Ratio
  
  5. Sortino Ratio
  
  6. Maximum Drawdown
  
  7. Correlation Heatmaps

  Stress-period performance analysis

**7. Results & Outcomes**
  Key Performance Metrics
  
    a.Sharpe Ratio: ~1.06
    
    b. Sortino Ratio: ~1.34
    
    c. Annualized Volatility: ~18%
    
    d. Maximum Drawdown: ~31%
  
  The portfolio demonstrates stable risk-adjusted performance over long horizons.

**Stress Test: COVID-19 (Feb–Apr 2020)**

1. Sharp drawdown during market crash

2. Gradual recovery post-crisis

3. Diversification across asset classes helped limit downside risk

4. This highlights the resilience of risk parity under extreme volatility.

**Folder Structure**
├── Portfolio_building.ipynb     # Core notebook: data processing, modeling, backtesting
├── Arbitrage_Arena_Risk_Parity_Portfolio_Report.pptx
├── README.md

**Key Learnings**
Risk-based allocation can outperform naive diversification during volatile regimes

Avoiding return prediction improves robustness and interpretability

Correlation and volatility are powerful signals for portfolio construction

Stress testing is essential for understanding real-world behavior

**Future Improvements**
Regime-aware or volatility-adaptive allocation

Periodic portfolio rebalancing

Transaction cost modeling

Comparison with mean-variance optimization

**Final Note**
This project reflects my approach to analytical problem-solving: prioritizing clarity, robustness, and reasoning over complexity. It was built to be interpretable, reproducible, and resilient rather than optimized for short-term gains.
