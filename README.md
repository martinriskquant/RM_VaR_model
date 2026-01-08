# RM_VaR_model
Intro: VaR as known as (Value at Risk). VaR is a popular risk metric used to measure the overall portfolio risk exposure over a specified period in the banking and financial industries.

Modeling Direction:
  1. Historical Approach
     - linear portfolio
       Based on the historical change of the Spot price for each underlying in your portfolio under a 250-day window to project the portfolio valuee change 
     - Non-linear portfolio
       Based on
  3. Variance-Covariance Approach
  4. Monte Carlo Approach
     - Case 1: assume the underlyings under the portfolio follow a joint distribution with a Gaussian copula.
     - Case 2: assume the underlyings under the portfolio follow a joint distribution with a T-Distribution copula. (captured more tail risk than the Gaussian copula)
  Note that the Gaussian copula refers to the Wiener process under the GBM.
    - Case 3: time series model fit in for Spot changes and do the monte carlo

VaR backtesting:

Stress VaR (SVaR):
Stressing period:


Conditonal VaR:
