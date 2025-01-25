# Transaction-Cost-Analysis-Framework-for-Corporate-Bond-Trading-in-Python
## Overview
This project replicates the methodologies and findings of a research paper focused on **Transaction Cost Analysis (TCA)** for corporate bond trading from the perspective of retail investors. It evaluates the execution performance of transactions using the **Enhanced TRACE dataset** from 2015 to 2016. 

The TCA measures both:
- **Illiquidity costs** via bid-ask spreads.
- **Price impact dynamics** through mid-price movement.

The study provides insights into the liquidity and execution costs of corporate bond transactions and offers a robust benchmark for retail investors.

---

## Key Objectives
1. **Transaction Initiator Estimation**: 
   - Identify whether a trade is buyer-initiated or seller-initiated (missing in the TRACE dataset).

2. **Bid-Ask Spread Analysis**:
   - Estimate bid-ask spreads to measure liquidity costs.
   - Use regularized regression models to identify significant bond-specific features influencing transaction costs.

3. **Mid-Price Dynamics Analysis**:
   - Study the transient price impact of trades, including:
     - Initial price jumps.
     - Price decay patterns.
     - Stabilization to a permanent price level reflecting the trade's informational content.
   - Highlight asymmetries in price impacts for buy- and sell-initiated transactions.

---

## Methodology
1. **Data Preprocessing**:
   - Use Enhanced TRACE data for corporate bond transactions.
   - Derive transaction initiators (buy or sell) based on trade features.

2. **Regression Analysis**:
   - Apply regularized regression models (Lasso, Ridge, Elastic Net) to determine key factors affecting bid-ask spreads.
   - Analyze variables such as bond price volatility, years to maturity, and trade volume.

3. **Transient Impact Model (TIM)**:
   - Estimate price impact kernels using non-parametric methods.
   - Assess trade-specific impacts and identify decay and stabilization patterns.

---

## Dataset Description
The Enhanced TRACE dataset includes:
- Trade-level details of corporate bonds.
- Missing fields like transaction initiator, estimated using model-based techniques.
- Features analyzed:
  - Volatility of bond prices.
  - Years from issue date.
  - Trade frequency and amount.

---

## Tools and Technologies
- **Programming Languages**: Python
- **Libraries**:
  - pandas, numpy, scikit-learn for data processing and regression.
  - matplotlib, seaborn for data visualization.
- **Models**:
  - Lasso, Ridge, Elastic Net regression.
  - Transient Impact Model (TIM) for price dynamics.

---

## Future Work
- Get additional data to extend the number of predictors and apply regularized regression models, tree-based models and neural networks.
- Incorporate more sophisticated models for transaction initiator estimation.
- Explore the impact of market-wide shocks on corporate bond liquidity.

---

## References
1. Transaction cost analytics for corporate bonds by XIN GUO, CHARLES-ALBERT LEHALLE, and RENYUAN XU (2022)
2. Hendershott, T., & Madhavan, A. (2015).
3. Dick-Nielsen, J., et al. (2012).
4. Goldstein, M., et al. (2007).
5. Enhanced TRACE dataset documentation.
