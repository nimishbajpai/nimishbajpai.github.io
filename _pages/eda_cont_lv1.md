---
layout: single
title: "EDA: Continuous Variables"
permalink: /eda_cont_lv1/
author_profile: false
---

This section provides a visual exploration of the key continuous variables used in the credit risk model. Each variable is analyzed for distribution and skewness, helping guide preprocessing decisions like binning, transformation, and outlier treatment.

---

## CSCORE_B (Borrower Credit Score)

![CSCORE_B](/assets/images/eda_cont_lv1/cont_eda_CSCORE_B.png)

- The distribution is right-skewed with a concentration in the 700–800 range.
- A long tail is observed towards the lower score segment, with very few borrowers under 600.
- Binning may help convert this into a more stable feature across different risk bands.

---

## ORIG_RATE (Original Interest Rate)

![ORIG_RATE](/assets/images/eda_cont_lv1/cont_eda_ORIG_RATE.png)

- The most common rates lie between 4% and 6%.
- Sharp peaks around 4.75% and 5.25% indicate rounding or standard rate structures.
- Could be binned into rate bands or treated using smoothing techniques.

---

## ORIG_TERM (Original Loan Term)

![ORIG_TERM](/assets/images/eda_cont_lv1/cont_eda_ORIG_TERM.png)

- Strong spike at 360 months (30 years), which is a standard mortgage term.
- Smaller bumps at 180 and 240 months suggest presence of non-standard or custom loan terms.
- Likely to be more useful as a binned or categorical variable.

---

## OLTV (Original Loan-to-Value)

![OLTV](/assets/images/eda_cont_lv1/cont_eda_OLTV.png)

- Major spike at 80%, indicating an industry threshold for high-risk categorization.
- Distribution is slightly right-skewed with a fair amount of loans between 70% and 90%.
- Outliers beyond 100% could indicate second mortgages or data issues.

---

## OCLTV (Original Combined Loan-to-Value)

![OCLTV](/assets/images/eda_cont_lv1/cont_eda_OCLTV.png)

- Similar to OLTV, but includes secondary liens.
- High concentration around 80%, again suggesting underwriting limits or LTV thresholds.
- May require capping or binning for model stability.

---

## DTI (Debt-to-Income Ratio)

![DTI](/assets/images/eda_cont_lv1/cont_eda_DTI.png)

- Relatively symmetric distribution centered around 35–40.
- Tail extends beyond 50, suggesting possible high-risk segments.
- Normalization or banding could enhance modeling.

---

## MI_PCT (Mortgage Insurance Percentage)

![MI_PCT](/assets/images/eda_cont_lv1/cont_eda_MI_PCT.png)

- Strong multimodal distribution with clear spikes at 25%, 30%, and 35%.
- Suggests industry-standard MI structures.
- Retaining as-is or grouping these spikes may yield useful predictive power.