# primetrade_assignment
the technical assignment of primetrade for data_science internship
# Trader Performance vs Market Sentiment Analysis

## Objective

Analyze how Bitcoin market sentiment (Fear vs Greed) influences trader behavior and performance on Hyperliquid, and identify actionable strategy insights based on regime conditions.

---

## Methodology

### Data Preparation
- Standardized column names and cleaned missing values.
- Converted trade timestamps to daily granularity.
- Merged trade data with daily Fear/Greed sentiment classification.
- Engineered daily trader-level metrics:
  - Daily realized PnL
  - Win rate
  - Number of trades per day
  - Average trade size
  - Trader volatility (standard deviation of daily PnL)

### Analytical Approach
- Compared trader performance across Fear and Greed regimes.
- Evaluated behavioral shifts in trade frequency and win rate.
- Segmented traders into:
  - High vs Low activity groups
  - Consistent vs Volatile traders
- Assessed how different trader segments respond to sentiment regimes.

---

## Key Insights

1. **Performance is Regime-Dependent**  
   Trader profitability differs across sentiment regimes. Greed periods tend to show stronger average returns but also higher variability, indicating increased risk exposure during bullish sentiment phases.

2. **Behavioral Expansion During Greed**  
   Traders increase activity during Greed regimes. However, win rate improvements are not proportional to the increase in trading frequency, suggesting possible overconfidence-driven trading behavior.

3. **Segment Sensitivity to Sentiment**  
   High-activity and volatile traders exhibit greater downside exposure during Fear regimes compared to low-activity or consistent traders. Aggressive trading styles amplify regime-based risk.

Overall, market sentiment acts as a regime filter that influences both trader behavior and risk-adjusted performance.

---

## Strategy Recommendations

### Strategy 1 – Sentiment-Based Risk Moderation
During Fear regimes, reduce exposure for high-activity traders through trade frequency limits or leverage moderation.  
Rationale: This segment demonstrates elevated downside volatility under negative sentiment conditions.

### Strategy 2 – Overtrading Control During Greed
Implement trade frequency caps during Greed regimes to prevent excessive variance without proportional improvement in win rate.  
Rationale: Increased activity does not consistently translate into improved profitability.

These strategies can be implemented as a regime-based risk overlay in execution systems.

---

## Bonus – Predictive Model

A Random Forest classifier was trained to predict daily trader profitability using sentiment and behavioral features.  

Results indicate limited but measurable predictive capability. Feature importance analysis shows that behavioral metrics such as trade frequency and win rate contribute more predictive signal than sentiment classification alone.

This suggests that trader behavior carries meaningful predictive information beyond sentiment regime indicators.

---

## Repository Structure

- `Data_Scientiest.ipynb` – Full analysis notebook
- `README.md` – Project summary and findings

---

## Tools Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
