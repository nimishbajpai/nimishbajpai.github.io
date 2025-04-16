---
layout: single
title: "EDA Level 2: Deep-Dive Analysis"
permalink: /eda-level2/
---

This deep-dive explores loan default behavior across dimensions like occupancy, credit score bands, DTI, OLTV, etc (All amounts in USD Bn).


---
### Origination Volume 

![Origination Amount](/assets/images/eda_cat_lv2/orig_amt.png)
 Origination volumes peaked sharply in 2009 across all quarters, with Q2 2009 showing the highest activity. This reflects the post-crisis refinancing boom when interest rates were slashed, and policy support was high. Volumes were also relatively strong in 2010, especially in Q3, before beginning a steady decline—likely due to tighter lending standards and market normalization after the housing crisis. Q2 consistently shows higher origination activity across years, possibly reflecting seasonal lending cycles or operational factors in the mortgage industry.   


---

### Occupancy Status

![Origination by Default Year and OCC_STAT](/assets/images/eda_cat_lv2/OCC_STAT_def.png)

 Most defaults stemmed from loans issued to primary occupants (`P`), while secondaries (`S`) and investors (`I`) had minimal exposure.

---

![Origination by Origination Year and OCC_STAT](/assets/images/eda_cat_lv2/OCC_STAT_orig.png)

 Loan origination peaked in 2009–10, with primary residence loans dominating the market.

---

### Customer Credit Score Band

![Default Amount by Customer Band](/assets/images/eda_cat_lv2/cust_band_default.png)

 Prime and subprime customers accounted for most defaults. Surprisingly, even subprime originations increased post-2008.
 For reference, below is the band-score mapping used in this analysis:
 Poor: <600,
 Subprime: 600-660,
 Prime: 660-720,
 Excellent: 720+


---

![Origination Amount by Customer Band](/assets/images/eda_cat_lv2/cust_band_orig.png)

 From 2004 to 2009, lending to subprime customers surged. Post-crisis, lenders shifted back to prime and excellent bands.

---

### Year of Origination

![Origination Amount of Default Accounts](/assets/images/eda_cat_lv2/def__by_orig_amt.png)

 Loans originated between 2005–2008 saw the highest default volume, especially in Q4, hinting at riskier year-end disbursements.

---


![Default Amount by Year](/assets/images/eda_cat_lv2/def_amt.png)

 Defaults peaked between 2009–2011—lagging the origination surge of 2005–08. The lag reflects the time between disbursement and delinquency.

---

###  Debt-to-Income (DTI) Band

![Default by DTI Band](/assets/images/eda_cat_lv2/DTI_BAND_def.png)

 Borrowers with DTI >40% made up a large chunk of defaults, though missing DTI values remain a concern.

---


![Origination by DTI Band](/assets/images/eda_cat_lv2/DTI_BAND_orig.png)

 Loans were generously issued to borrowers with 30–50% DTI, which typically indicates moderate risk. Higher DTI bands remain under scrutiny.

---

### First-Time Buyers

![Default by First Flag](/assets/images/eda_cat_lv2/FIRST_FLAG_def.png)

 Most defaults came from non-first-time buyers. First-time buyers did contribute meaningfully post-2008, indicating potential stress from new entrants.

---


![Origination by First Flag](/assets/images/eda_cat_lv2/FIRST_FLAG_orig.png)

 Majority of loans were issued to non-first-time buyers. However, the spike in first-time buyer originations in 2009–10 shows growing inclusivity post-crisis.


### Loan Term

Loans with longer terms (300–400 months) dominate originations and defaults across the years, indicating borrower preference or lender availability of long-term amortizations.

![Term Origination](/assets/images/eda_cat_lv2/TERM_BAND_orig.png)
![Term Default](/assets/images/eda_cat_lv2/TERM_BAND_def.png)

---

## Loan-to-Value (OLTV) Band

Loans with OLTV ratios between 80–90% represent the largest share of both originations and defaults, pointing to a risk band that is aggressively used and possibly underpriced during 2004–2010.

![OLTV Origination](/assets/images/eda_cat_lv2/OLTV_BAND_orig.png)
![OLTV Default](/assets/images/eda_cat_lv2/OLTV_BAND_def.png)

---

## Property Type (PROP)

Single Family homes (SF) form the bulk of loans, both in origination and default. Planned Unit developments (PU) and Condominiums (CO) follow at a distance.

![PROP Origination](/assets/images/eda_cat_lv2/PROP_orig.png)
![PROP Default](/assets/images/eda_cat_lv2/PROP_def.png)

---

## Loan Purpose

The majority of defaults occurred in loans taken for home purchases (C) and property improvement (P), though refinancing (R) also contributed significantly during 2009–2011.

![PURPOSE Origination](/assets/images/eda_cat_lv2/PURPOSE_orig.png)
![PURPOSE Default](/assets/images/eda_cat_lv2/PURPOSE_def.png)

---

## Interest Rate Bands

Defaults were highest in the 5.5%–6.5% interest rate band, reflecting the rate structure of that era. These were the most commonly issued loans pre-2010.

![Rate Origination](/assets/images/eda_cat_lv2/RATE_BAND_orig.png)
![Rate Default](/assets/images/eda_cat_lv2/RATE_BAND_def.png)

