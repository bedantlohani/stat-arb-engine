# Statistical Arbitrage Pairs-Trading Engine (US Equities, ESG-Themed vs. Baseline)

**May 2025 – Jul 2025**

A market-neutral strategy backtester that pairs “green” and “brown” universes constructed from S&P 500 stocks and Yahoo ESG scores, plus a vanilla same-sector baseline.

---

## 🚀 Project Overview

- **Objective:** Build and evaluate a mean-reversion pairs-trading engine using cointegrated spreads under realistic transaction costs, and compare performance against SPY.
- **Universes:**
  - **Brown:** Bottom-quartile Energy stocks by ESG “sustainability” score  
  - **Green:** Top-quartile Utilities + IT stocks by ESG  
  - **Baseline:** Vanilla same-sector pairs
- **Key Steps:**  
  1. **Data Ingestion & Cleaning**  
     - Download and align S&P 500 adjusted close prices  
     - Fetch daily Yahoo ESG scores  
  2. **Universe Construction & Filtering**  
     - Classify stocks into brown/green sets  
     - Pre-filter candidate pairs by Pearson correlation (ρ ∈ [0.60, 0.80])  
  3. **Cointegration & Signal Generation**  
     - Run Engle–Granger two-step test  
     - Estimate hedge ratios via OLS  
     - Compute spread Z-score and generate entry/exit signals  
  4. **Backtest & Analysis**  
     - Simulate long/short positions with realistic transaction costs  
     - Produce threshold-sensitivity heatmaps, trade-level blotters  
     - Compute performance metrics (Sharpe, CAGR, max drawdown, win rate)  

---

