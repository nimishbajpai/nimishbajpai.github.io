---
layout: single
title: "Model Evaluation - Logistic Regression"
permalink: /model-results/
---

This page presents the key evaluation metrics and visualizations for the logistic regression model built to predict loan defaults.

---

## 1. ROC Curve

![ROC Curve](/assets/images/results/roc.png)

The ROC curve illustrates the trade-off between the true positive rate (recall) and false positive rate for various threshold values. The AUC (Area Under the Curve) is **0.780**, indicating a reasonably good ability to discriminate between default and non-default loans. A value of 0.5 would imply random guessing, and 1.0 is a perfect model. Our model, with an AUC of 0.780, is significantly better than random.

---

## 2. Calibration Curve

![Calibration Curve](/assets/images/results/calib.png)

The calibration curve shows how well the predicted probabilities from the logistic regression model align with actual observed default rates. A well-calibrated model should have points close to the 45-degree reference line. Our model tracks closely up to a predicted probability of ~0.6, after which it starts to slightly underestimate default probabilities. This suggests decent calibration within the core probability range.

---

## 3. Confusion Matrix

![Confusion Matrix](/assets/images/results/cm_mat.png)

The confusion matrix provides an overview of correct and incorrect classifications at the selected threshold (0.5):

- **True Negatives (TN):** 302,582  
- **False Positives (FP):** 98,534  
- **False Negatives (FN):** 18,534  
- **True Positives (TP):** 37,265

This results in:
- **Accuracy:** 0.74  
- **Precision:** 0.274  
- **Recall (TPR):** 0.668  
- **False Positive Rate (FPR):** 0.245

The model correctly identifies a large portion of actual defaulters, but at the cost of a relatively high number of false positives.

---

## 4. Precision-Recall vs Threshold

![Precision vs Recall](/assets/images/results/prec_v_rec.png)

This plot shows how precision and recall vary with different decision thresholds. As the threshold increases:
- **Precision increases**: We become more confident in labeling a loan as default, but...
- **Recall decreases**: We miss more actual defaulters.

This trade-off is important in real-world applications. A threshold of 0.5 gives decent recall but lower precision. Depending on business context (e.g., cost of false positives vs false negatives), the threshold can be adjusted.

---

## Summary

The logistic regression model demonstrates:
- Solid discriminative power (AUC = 0.78)
- Reasonable calibration
- Strong recall but modest precision at default threshold
- Predictive power that can be enhanced through threshold tuning or more complex models