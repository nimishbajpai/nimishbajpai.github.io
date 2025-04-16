---
layout: single
title: "Lifetime PD Model Summary"
permalink: /pd-summary/
author_profile: false
---

## 🧾 Project Overview

This project develops a lifetime probability of default (PD) model using the publicly available Fannie Mae Single-Family Loan Performance dataset, focusing on Wells Fargo loans originated from 2004 to 2010, and subsequently acquired by Fannie Mae. The goal is to estimate the likelihood that a loan will go 90+ days delinquent over its lifetime, aligning with IFRS 9-style credit risk modeling.

The analysis begins with structured exploratory data analysis (EDA), followed by feature binning and transformation using Weight of Evidence (WOE). A logistic regression model is then trained on the transformed features to estimate default probabilities.

Key evaluation metrics include:

AUC (ROC): ~0.74 — indicating good discriminatory power

KS Statistic: ~0.36 — showing effective rank-ordering

Calibration curve: Confirms the model is well-aligned with observed default rates

This clean, pre-2010 mortgage data — relatively untouched by post-crisis regulatory overlays — offers a unique opportunity to model organic credit behavior. The project also sets up the foundation for building scorecards or integrating macroeconomic overlays in future stages.

---

### ROC Curve
![ROC Curve](/assets/images/roc.jpg)

### Calibration Curve
![Calibration Curve](/assets/images/calibration.jpg)

---

## 🔍 EDA Summary

The dataset consists predominantly of owner-occupied, single-unit homes, with loans primarily originated via retail and correspondent channels. California and Texas contribute significantly to origination volumes, indicating regional concentration that may warrant separate modeling.

Origination volumes peaked in 2009–2010, driven by loans with high original terms (360 months), moderate origination rates (5–6%), and OLTV ratios mostly between 80–90%. Borrower credit scores are largely in the 700–800 range, indicating a generally prime-quality loan book.

Default behavior shows strong patterns, especially in loans with:

- Higher OLTV (above 90%)

- DTI ratios above 40

- Lower credit scores (<700)

- Higher origination rates (6.5% and above)

- PURPOSE = Cash-out refinance 

Continuous variable distributions reveal clear skews — for example, OCLTV and OLTV are clustered around 80, and MI_PCT exhibits strong banding, suggesting insurer rules or thresholds. The DTI distribution shows a steep drop beyond 45, aligning with typical underwriting cutoffs.

EDA Level 2 further revealed:

- Defaults are more pronounced in property types like MH (manufactured housing) and PU (planned urban development).

- Loans originated through wholesale channels have notably higher default rates compared to retail or correspondent.

Overall, the portfolio is well-suited for modeling, with clear patterns of risk emerging across time, borrower profile, loan terms, and product types. 



---

## 🔗 Detailed Analysis

- [Level 1 EDA on Categorical features](/eda-dashboard/)
- [Level 1 EDA on Continuous features](/eda_cont_lv1/)
- [EDA Level 2 Insights](/eda-level2/)
- [Model Results](/model-results/)
