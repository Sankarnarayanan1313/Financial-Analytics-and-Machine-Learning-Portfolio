# Retail Portfolio Loss Estimation & Risk Strategy for Unsecured Lending

Project Overview

This project focuses on building a risk framework to estimate probability of default (pd) using borrower level behavioral and credit variables. logistic regression was used for modeling, and the classification threshold was adjusted to better capture high risk accounts. expected loss (el) was then calculated using pd along with ead and lgd, and the portfolio was analyzed across segments to understand risk distribution. stress testing was performed by worsening key variables like delinquencies, utilization, dti and credit score to evaluate how losses increase under adverse conditions.

### Table Of Contents
1. [Data Wrangling](#Data-Wrangling)
2. [Model Building](#Model-Building)
3. [Expected Loss (EL) Analysis](#Expected-Loss-(EL)-Analysis)
4. [Portfolio Stress Testing](#Portfolio-Stress-Testing)

## What was done
- Data cleaning and feature engineering using Pandas
- Built PD model using Logistic Regression
- Estimated Expected Loss (PD × EAD × LGD)
- Performed portfolio analysis (DPD buckets, PD segments, cohort/vintage trends)
- Conducted stress testing and migration analysis

## Key insights
- Default rate ~7.75% indicating moderate portfolio risk
- EWS segment ~16% showing early risk signals
- High-risk segments (~23%) contribute ~70%+ of total loss
- Stress scenario leads to ~16.6% increase in Expected Loss

## Tools used
- Python (Pandas, NumPy)
- Scikit-learn
- Matplotlib, Seaborn