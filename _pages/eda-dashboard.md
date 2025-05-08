---
layout: single
title: "Exploratory Analysis: Fannie Mae Loan Data"
permalink: /eda-dashboard/
author_profile: false
---


The Fannie Mae loan dataset reflects a primarily low-risk portfolio. Most loans are for single-family, owner-occupied homes — a typical and stable segment. Borrowers are largely experienced, with one or two co-borrowers, and loans tend to be originated through retail and correspondent channels, with minimal presence from brokers.

The distribution across loan purposes shows a balance between purchases, rate-term refinances, and cash-out refinances — the latter being potentially riskier due to equity extraction. Mortgage insurance is present but concentrated in one type, and loan modifications are rare, suggesting portfolio stability.

Geographically, a few states like California, Texas, and Florida dominate origination volume, introducing regional concentration risk. Overall, the dataset shows a clean, structured book of business with consistent patterns, making it well-suited for predictive credit risk modeling.

---

## 1. OCC_STAT (Occupancy Status)

![OCC_STAT](/assets/images/eda_cat_lv1/EDA1_OCC_STAT.png)

 
The bulk of the loan book is focused on owner-occupied primary residences (denoted by code 'P') — typically associated with lower default risk and stronger borrower commitment. 

---

## 2. PROP (Property Type)

![PROP](/assets/images/eda_cat_lv1/EDA1_PROP.png)

  
Single-family homes make up the core product. Manufactured homes may carry higher risk.

---

## 3. PURPOSE (Loan Purpose)

![PURPOSE](/assets/images/eda_cat_lv1/EDA1_PURPOSE.png)

  
This is a well-diversified mix of loan purposes. Cash-out refinance loans may require deeper monitoring due to higher equity extraction behavior.

---

## 4. STATE (Loan Volume by State)

![STATE](/assets/images/eda_cat_lv1/EDA1_STATE.png)

  
Strong concentration in CA, TX, FL, and NJ. Regional economic changes could significantly affect performance.So if a state-wise analysis is to be performed (outside of the scope of this project), state-level segmentation would be the starting point.

---

## 5. CHANNEL (Origination Channel)

![CHANNEL](/assets/images/eda_cat_lv1/EDA1_CHANNEL.png)

  
Correspondent and Retail are dominant. Broker-sourced loans are fewer, and may warrant separate risk profiling.

---

## 6. FIRST_FLAG (First-Time Homebuyer)

![FIRST_FLAG](/assets/images/eda_cat_lv1/EDA1_FIRST_FLAG.png)

  
Mostly repeat buyers, suggesting a seasoned borrower base. First-time homebuyers could be more vulnerable in stress conditions.

---

## 7. MI_TYPE (Mortgage Insurance Type)

![MI_TYPE](/assets/images/eda_cat_lv1/EDA1_MI_TYPE.png)

  
Most loans carry MI Type 1. Understanding risk distribution by MI type can support better loss forecasting.

---

## 8. MOD_FLAG (Modification Flag)

![MOD_FLAG](/assets/images/eda_cat_lv1/EDA1_MOD_FLAG.png)

  
Few loans have been modified, indicating most are in original contractual state — useful for modeling unaltered behavior.

---

## 9. NO_UNITS (Number of Units)

![NO_UNITS](/assets/images/eda_cat_lv1/EDA1_NO_UNITS.png)

  
Nearly all loans are for single-family residences, reinforcing the dataset’s alignment with traditional residential lending.

---

## 10. NUM_BO (Number of Borrowers)

![NUM_BO](/assets/images/eda_cat_lv1/EDA1_NUM_BO.png)

  
1-2 borrower structure is standard. Joint borrowers may carry lower credit risk — this could be a valuable feature in modeling.

---
