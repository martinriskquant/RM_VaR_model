## RM_VaR_model



### Value at Risk (VaR)
Value at Risk (VaR) is a widely used risk measure in finance that estimates the potential loss in the value of a portfolio over a defined time horizon at a given confidence level. Formally, at a confidence level of $(1 - \alpha)$ (e.g., 95% or 99%), VaR is the maximum expected loss such that the probability of a larger loss is at most $\alpha$ (e.g., 5% or 1%). For example: 99% 1-Day VaR = 1M, With 99% confidence, the portfolio will not lose more than 1M amount over next 1 Day.

### Conditional Value at Risk (CVaR)
Conditional Value at Risk (CVaR), also known as **Expected Shortfall (ES)** or **Tail VaR**, is a risk measure that addresses the limitations of VaR by quantifying the expected loss in the worst $\alpha$ cases (i.e., beyond the VaR threshold). It represents the average loss given that the loss exceeds the VaR level. For example: 99% 1-Day CVaR = 1.5M, If the worst-case scenario (exceeding VaR) occurs, the expected loss (average loss) is the 1.5M amount.

**Difference between VaR and CVaR**\
VaR provides a threshold for potential losses but does not indicate the severity of losses beyond that threshold.


### VaR and CVaR Modeling Direction:
  1. Historical Approach
     - Linear portfolio & Non-linear portfolio
       Based on the historical change of the risk factor for each instrument in your portfolio under a look-back time window (default is 2 years according to Basel standard and industry practise: is around 2yr -5yr) to project the portfolio value change. The simulated portfolio value change is the simulated PnL for the pre-defined time horizon. Based on the confidence level you defined, the VaR is the percentile(1-confidence interval)
        - Possible risk factors: Spot price, FX spot price, Interest rate, Credit spread, Implied Vol, etc., which depend on your instrument in your portfolio
   
  2. Variance-Covariance Approach
    
  3. Monte Carlo Approach
     - General Case: Stock price is following GBM --> $$dS_t = \mu S_t \, dt + \sigma S_t \, dW_t$$ 
       - Case 1: assume the underlyings under the portfolio follow a joint distribution with a Gaussian copula.
       - Case 2: assume the underlyings under the portfolio follow a joint distribution with a T-Distribution copula. (captured more tail risk than the Gaussian copula)
     - Possible Case: Stock price is following a Time series model eg ARIMA-GARCH
       - Case 3: time series model fit in for Spot changes and do the Monte Carlo


### Stress VaR (SVaR):
Stress period:
- 2007-2008 crisis
- 2020-2022 COVID

### VaR backtesting:


#### Key question????
How to set up the limit for monitoring the risk ?
- Based on your own capital to set certian % like 5% of total capital and your stragety risk and return ratio
- Based on the nature of your company. If you are bank, there is a capital charge from Regulator. Your VaR limit can be restricted by the RWA
