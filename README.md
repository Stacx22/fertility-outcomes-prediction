# Fertility Outcomes Prediction

### Overview
Predictive modeling project exploring health and lifestyle-driven factors affecting fertility outcomes. Built in R using tidymodels to compare multiple supervised learning algorithms.

### Business / Healthcare Problem
Growing infertility rates pose clinical and economic challenges. Identifying risk indicators supports earlier education and intervention.

### Data
- Source: UCI Machine Learning Repository — Fertility Diagnosis dataset
- Rows: 100 | Target: Altered vs. Normal fertility

### Methods
- Preprocessing with `recipes`
- Models: Logistic Regression, Random Forest, XGBoost
- Metrics: ROC AUC, F1, Precision–Recall
- Class balance handling using `themis::step_upsample`

### Results
- XGBoost performed best (AUC = 0.91)
- Smoking, alcohol consumption, and age were top predictive drivers

> See `/docs/Fertility_Model_Illustrations.pdf` for visuals

### How to Run
```r
source("fertility_model.R")
