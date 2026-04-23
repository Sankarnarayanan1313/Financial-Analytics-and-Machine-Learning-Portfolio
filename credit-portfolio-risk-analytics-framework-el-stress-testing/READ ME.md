# Credit Portfolio Risk Analytics Framework - EL Estimation & Stress Testing

Project Overview

This project is to develop a corporate credit portfolio risk framework to estimate probability of default (PD) using credit ratings as a proxy target variable. Used Logistic Regression and evaluated model performance using ROC-AUC, Gini Coefficient, KS Statistic, and PSI. Adjusted classification threshold to improve identification of high-risk companies. Estimated Expected Loss (EL) using model outputs and analyzed portfolio risk under different stress scenarios.

### Table Of Contents

Target Variable already Defined as Default_risk_indicator. For more Information, Please refer to the **"Data Preprocessing.ipynb"** notebook

1. [Calculation of WoE and IV using OptimalBinning](#Calculation-of-WoE-and-IV-using-OptimalBinning)
2. [Model Construction and Evaluation](#Model-Construction-and-Evaluation)
   - 2.1 [Logistic Regression](#Logistic-Regression)
   - 2.2 [Precision, Recall and Threshold Analysis](#Precision,-Recall-and-Threshold-Analysis)
   - 2.3 [Confusion Matrix](#Confusion-Matrix)
   - 2.4 [ROC Curve and AUC](#ROC-Curve-and-AUC)
3. [Model Validation metrics](#Model-Validation-metrics)
   - 3.1 [KS Statistic](#KS-Statistic)
   - 3.2 [Gini Coefficient](#Gini-Coefficient)
   - 3.3 [Population Stability Index (PSI)](#Population-Stability-Index-(PSI))
4. [Coefficients Interpretation](#Coefficients-Interpretation)
   - 4.1 [Sector Coefficient Breakdown](#Sector-Coefficient-Breakdown)
5. [Expected Loss Calculation](#Expected-Loss-Calculation)
   - 5.1[Expected Loss sectoral analysis](#Expected-Loss-sectoral-analysis)
6. [Portfolio Stress Testing](#Portfolio-Stress-Testing)
   - 6.1 [Expected Loss Distribution in Baseline and Stress Scenarios](#Expected-Loss-Distribution-in-Baseline-and-Stress-Scenarios)
   - 6.2 [Expected Loss Migration Matrix](#Expected-Loss-Migration-Matrix)
   - 6.3 [Top Borrowers with Largest Expected Loss Increase](#Top-Borrowers-with-Largest-Expected-Loss-Increase)
   - 6.4 [Sector-wise EL change under Stress](#Sector-wise-EL-change-under-Stress)
7. [Model Conclusion](#Model-Conclusion)


# Coefficent Interpretation

Cash Ratio (-0.874) and Operating Cash Flow to Sales Ratio (-0.642): Higher liquidity and stronger cash flow from sales significantly reduce the probability of high default risk, indicating financially stable firms are less likely to fall into distressed credit ratings.

Sector (-0.612) and Operating Cash Flow per Share (-0.474): Default risk varies across industries, and companies generating stronger cash flow per share are less likely to be classified in high default-risk rating categories.

Return on Assets (-0.432) and Debt-Equity Ratio (-0.394): Firms that utilize their assets efficiently and maintain healthier capital structures tend to have lower chances of being rated in high default-risk categories.

Gross Profit Margin (-0.335) and Free Cash Flow to Operating Cash Flow Ratio (-0.311): Higher profitability and better cash flow conversion reduce the likelihood of firms falling into high default-risk rating groups rather than actual default events.

## Sector Coefficient Breakdown


**High Risk Sectors**
Consumer Services: Firms in this sector show a higher likelihood of falling into high default-risk rating categories because revenues depend heavily on discretionary consumer spending, which declines during economic downturns.

Basic Industries: Companies in this sector tend to have higher default-risk ratings due to their strong dependence on commodity price cycles and overall economic conditions.

Technology & Consumer Durables: Firms in these sectors show slightly higher default-risk classification because demand for technology products and durable goods is cyclical and sensitive to consumer purchasing power.

**Low Risk Sectors**

Public Utilities: Companies in this sector are less likely to fall into high default-risk rating groups because they typically operate with stable and regulated revenue streams.

Consumer Non-Durables: Firms producing essential goods show lower default-risk ratings since demand for necessities remains relatively stable even during economic downturns.

Finance & Miscellaneous: Firms in these sectors tend to have lower default-risk classification as financial institutions often maintain stricter capital requirements and liquidity management practices.

# **Model Conclusion**

**Proxy target variable**: Credit ratings were used as a proxy for default risk instead of actual default events, which may not fully capture true default behavior.

**Proxy variables for LGD and EAD**: Due to limited data availability, Debt Ratio was used as an LGD proxy and Current Ratio as an EAD proxy, which may not perfectly represent actual exposure and recovery rates.

**Limited data scope**: The model can distinguish between high-risk and low-risk firms reasonably well, but its predictive performance may improve with more detailed financial information and real default data.