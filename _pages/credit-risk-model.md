---
title: "Lifetime PD Model Visual Summary"
permalink: /credit-risk-model/
layout: single
classes: wide
author_profile: false
---

# 📈 Visual Insights from EDA & Modeling

_This page summarizes key takeaways from visualizations used in EDA and model validation without showing code._

### 🖼️ Figure 1
Channel, occupancy status, and property type have skewed distributions. Majority of loans are owner-occupied and originated through retail channels — key for base segment profiling.

![Figure 1](/assets/images/figure_1.png)

---
### 🖼️ Figure 2
Loan origination peaked around 2007 before declining — helpful for understanding economic cycles in the dataset.

![Figure 2](/assets/images/figure_2.png)

---
### 🖼️ Figure 3
Defaults were more frequent in loans originated in 2006–2008, suggesting stress around the financial crisis.

![Figure 3](/assets/images/figure_3.png)

---
### 🖼️ Figure 4
Features like DTI, FICO, and OLTV have varying distributions. FICO is slightly right-skewed (good borrowers dominate), while OLTV has multiple modes.

![Figure 4](/assets/images/figure_4.png)

---
### 🖼️ Figure 5
Defaulted loans show higher OLTV and DTI and lower FICO scores — visually confirming the predictive power of these features.

![Figure 5](/assets/images/figure_5.png)

---
### 🖼️ Figure 6
Certain states show significantly higher default rates. This helps with region-based credit strategy segmentation.

![Figure 6](/assets/images/figure_6.png)

---
### 🖼️ Figure 7
Cash-out refinance and debt consolidation loans have higher delinquency — indicating behavioral risk beyond credit scores.

![Figure 7](/assets/images/figure_7.png)

---
### 🖼️ Figure 8
No severe multicollinearity observed. OLTV and OCLTV are highly correlated, but not redundant. Safe for logistic modeling.

![Figure 8](/assets/images/figure_8.png)

---
### 🖼️ Figure 9
Binned OLTV and DTI show smooth monotonic WOE trends, ideal for credit scorecard-style logistic regression.

![Figure 9](/assets/images/figure_9.png)

---
### 🖼️ Figure 10
The model is well-calibrated across probability bins. Predicted PD aligns closely with observed default rate.

![Figure 10](/assets/images/figure_10.png)

---
### 🖼️ Figure 11
AUC of ~0.74 shows reasonably strong separation between good and bad loans using logistic regression.

![Figure 11](/assets/images/figure_11.png)

---
### 🖼️ Figure 12
KS statistic around 0.36 indicates decent rank-ordering of risk — a key metric in retail credit models.

![Figure 12](/assets/images/figure_12.png)

---