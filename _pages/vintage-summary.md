---
title: "Vintage Default Visualisation"
permalink: /vintage-summary/
layout: single
author_profile: false
---


Conducted exposure-weighted vintage analysis using Fannie Mae single-family loan data (2004–2010).  
Built a quarterly vintage matrix of 90+ DPD defaulted UPB, and visualized cumulative default rates using a heatmap.

---

### Key Highlights

- Cleaned, joined and transformed 2000–2010 vintage Fannie Mae loan performance data for Wells Fargo loans
- Created flags for delinquency buckets (DLQ 1/2/3/4)
- Calculated months-to-default relative to origination
- Grouped by origination quarter to build a vintage-default matrix
- Normalized using original UPB* to calculate % defaulted
- Visualized using annotated seaborn heatmaps

*UPB: Unpaid Balance

---

### Output

<img src="/assets/images/vintage-analysis/vintage-heatmap.png" alt="Vintage Default Heatmap" style="border: 1px solid #ccc; border-radius: 8px;" />


---
### Key Takeaways

- 2006–2007 vintages experienced the highest cumulative default rates, peaking at 12–13% of original UPB, clearly reflecting pre-crisis underwriting risk.
- Post-2008 vintages show significantly improved performance with <2% default rates, likely due to tighter credit standards and policy intervention.
- Default rates were front-loaded, with the majority of defaults occurring within the first 24–36 months of loan origination.
- The heatmap visualization helps identify high-risk vintages and timing of deterioration at a glance — useful for portfolio monitoring and capital planning.
- Demonstrates a complete lifecycle view of mortgage portfolio risk using real-world delinquency data and custom Python visualization.

---

###  Tools Used

<img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white" alt="Python" />
<img src="https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white" alt="Pandas" />
<img src="https://img.shields.io/badge/Seaborn-3776AB?style=flat&logo=python&logoColor=white" alt="Seaborn" />
<img src="https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white" alt="Jupyter">

---

### 🔗 View Notebook

 <a href="https://github.com/nimishbajpai/nimishbajpai.github.io/blob/main/projects/vintage-analysis/vintage_analysis_final.ipynb" target="_blank">View full notebook on GitHub</a>