# 📊 Cross-Asset Portfolio Optimization using Risk Parity  
### Arbitrage Arena 2026 | Quantitative Finance Case Study

## 📌 Overview
This project focuses on building a diversified **cross-asset investment portfolio** using a **Risk Parity framework**. The objective is to maximize risk-adjusted returns while controlling volatility and drawdowns across different market regimes.  

The portfolio spans **equities, indices, and commodities**, emphasizing balanced risk contribution rather than return prediction.

---

## 🎯 Problem Statement
**Selected Problem:** Cross-Asset Portfolio Optimization  

### Objectives:
- Build a diversified portfolio across equities, index, and commodities  
- Maximize risk-adjusted returns  
- Control drawdowns during volatile market regimes  

---

## 📊 Dataset Overview

### Assets Used
- **Equities:** AAPL, MSFT, NVDA, AMZN, META, TSLA  
- **Index:** NASDAQ  
- **Commodities:** Gold, Silver, Crude Oil  

**Data Type:** Daily historical OHLC price data  
**Time Horizon:** ~11–12 years  

---

## 🧠 Data Preprocessing
- Timestamp standardization and alignment  
- Numeric conversion of OHLC values  
- Missing value handling using forward and backward fill  
- OHLC price visualization for validation  
- Computation of daily and log returns  

---

## 🔍 Exploratory Data Analysis
- Price trend inspection using OHLC charts  
- Return distribution analysis  
- Volatility clustering during crisis periods  
- Cross-asset correlation analysis to assess diversification benefits  

---

## ⚙️ Feature Engineering
- Rolling volatility as the primary risk feature  
- Correlation matrix for diversification assessment  
- Identification of low-correlation assets  
- Volatility-aware features designed for allocation stability  

---

## 🧮 Model Approach: Risk Parity Portfolio

wᵢ = (1 / σᵢ) / Σⱼ (1 / σⱼ)


### Constraints
- Fully invested (weights sum to 1)  
- Long-only positions  
- No leverage  
- Static allocation  

This approach improves robustness and reduces overfitting across market regimes.

---

## 🔄 Backtesting Framework
- Daily backtesting on aligned asset returns  
- Static risk parity weights  
- Portfolio returns calculated as weighted sum of asset returns  
- Transaction costs assumed to be zero  
- Portfolio value computed using cumulative compounding  

---

## 📈 Evaluation Metrics
- Annualized Return  
- Annualized Volatility  
- Sharpe Ratio  
- Sortino Ratio  
- Maximum Drawdown  
- Correlation Heatmap  
- Stress-test performance  

---

## 🧪 Backtest Results

### Key Performance Metrics
- **Sharpe Ratio:** ~1.06  
- **Sortino Ratio:** ~1.34  
- **Annualized Volatility:** ~18%  
- **Maximum Drawdown:** ~31%  

The portfolio demonstrates **stable risk-adjusted performance** across long-term market conditions.

---

## ⚠️ Stress Test: COVID-19 Period
- **Stress window:** Feb–Apr 2020  
- Sharp drawdown observed during market crash  
- Gradual recovery in post-crisis period  
- Cross-asset diversification helped limit downside risk  

---

## 💼 Business Impact

- Balanced risk exposure across asset classes  
- Reduced dependency on equity-only performance  
- Improved resilience during market stress  
- Suitable for investors prioritizing capital preservation with steady returns  

---

## 📸 Visualizations

### Portfolio Equity Curve
<img src="https://raw.githubusercontent.com/Sanskritid05/Arbitrage-Arena-2025/3365b00e22ecad597bc87f240128698cdc0e25ac/Screenshot%202026-02-22%20125838.png" width="800">

### Asset Correlation Heatmap
<img src="https://raw.githubusercontent.com/Sanskritid05/Arbitrage-Arena-2025/3365b00e22ecad597bc87f240128698cdc0e25ac/Screenshot%202026-02-22%20125604.png" width="700">

### 30-Days Rolling Volatility Analysis
<img src="https://raw.githubusercontent.com/Sanskritid05/Arbitrage-Arena-2025/3365b00e22ecad597bc87f240128698cdc0e25ac/Screenshot%202026-02-22%20125509.png" width="800">

*(Upload charts generated from the notebook into an `images/` folder)*

---

## 🛠 Tools & Technologies
- **Python** – Core analysis  
- **Pandas / NumPy** – Data manipulation  
- **Matplotlib** – Visualization  
- **Jupyter Notebook** – Experimentation & backtesting  

---

## 🔮 Conclusion & Future Work

### Conclusion
- Risk parity achieved balanced risk contribution across assets  
- Portfolio remained resilient under volatile regimes  
- Reduced drawdowns compared to concentrated equity exposure  

### Future Improvements
- Regime-aware dynamic allocation  
- Periodic rebalancing  
- Transaction cost modeling  

---

## 👤 Author
**Sanskriti Dutta**  
Arbitrage Arena 2025 – Prelims Submission

The portfolio is constructed using a **Risk Parity strategy**, where asset weights are determined by inverse volatility rather than expected returns.

