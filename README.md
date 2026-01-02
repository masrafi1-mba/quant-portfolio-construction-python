# Quantitative Portfolio Construction (Python)
## Overview
This repository implements an **end-to-end systematic investment framework** using Python.  
It translates core concepts from **quantitative finance and asset management** into a practical, executable workflow using real market data.

The project covers:
- Market return estimation
- Asset-level expected return modeling
- Factor-based filtering
- Portfolio optimization
- Risk-aware exit rules
- Historical backtesting with monthly rebalancing

The objective is to demonstrate how **financial theory can be operationalized into a repeatable investment process**, similar to workflows used in buy-side research and quantitative strategy teams.

---

## Project Workflow
The strategy follows a structured research-to-execution pipeline:

1. Estimate forward-looking market returns  
2. Model asset expected returns using CAPM and alpha  
3. Apply momentum-based universe filtering  
4. Optimize portfolio allocation under risk constraints  
5. Apply systematic exit and rebalance rules  
6. Evaluate performance through historical backtesting  

---

## Modules Description

### 1. Market Risk Premium – Forward (MRP Forward)
Estimates forward-looking market returns using earnings yield and growth assumptions.  
This serves as a macro-level expected return input for portfolio construction.

### 2. CAPM Analysis
Computes asset betas and expected returns relative to a market benchmark, providing a baseline risk–return model.

### 3. Alpha Estimation
Measures excess returns beyond CAPM expectations to identify securities with potential abnormal performance.

### 4. Momentum Filter
Applies trend and return-based momentum screening to construct an investable universe and filter out weak-performing assets.

### 5. Efficient Frontier Optimization
Constructs optimal portfolios using mean–variance optimization, including:
- Target monthly return constraints  
- Minimum volatility portfolios  
- Weight and diversification limits  

### 6. Exit Strategy
Implements systematic exit rules based on momentum deterioration, relative performance, and risk control signals.

### 7. Get Price
Generete Price of the stocks at the specific time

---

## Tools & Technologies
- Python  
- Pandas, NumPy  
- SciPy  
- yFinance  
- Matplotlib / Plotly  
- Jupyter Notebook  

---

## Disclaimer
This project is for **educational and research purposes only**.  
It does not constitute financial advice or an investment recommendation.

---

### A. Benchmark & Universe
- **Benchmark:** S&P 500  
- **Investment Universe:** S&P 200 (large-cap, liquid equities)

The benchmark is used for performance comparison and risk modeling, while the universe defines the eligible assets for portfolio construction.

---

### B. Portfolio Parameters
- **Holding & Review Frequency:** Monthly  
- **Number of Stocks:** 10–16  
- **Weight Constraints:**  
  - Maximum 12–15% per stock  
  - Sector exposure capped at 30%  
- **Rebalancing Frequency:** Monthly  

These constraints are designed to ensure diversification, control concentration risk, and maintain portfolio stability over time.

---

### C. Data Assumptions
- **Price Data:** Monthly closing prices  
- **Data History:** Minimum 5–10 years  
- **Risk-Free Rate:** 3-Month U.S. Treasury Bill  

Monthly frequency is chosen to balance signal stability, transaction costs, and practical portfolio management considerations.

---

### Rationale
The above assumptions reflect a **realistic, institutionally inspired portfolio setup**, emphasizing:
- Risk-adjusted returns rather than raw performance  
- Capital survivability through diversification and constraints  
- Reproducibility and robustness across market cycles  

These parameters are consistently applied across all modules, from expected return estimation to backtesting.

## Author
Maulana Asrafi  
Python • Quant Finance • Portfolio Optimization
