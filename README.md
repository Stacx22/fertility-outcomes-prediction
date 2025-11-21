# Fertility Outcomes Prediction

## Overview
This project uses supervised learning in R (tidymodels) to predict altered fertility outcomes based on lifestyle and health-related factors. The main goal is to identify which behaviors and medical history variables are most strongly associated with fertility risk while keeping the model interpretable for clinical use.

## Business / Healthcare Problem
Infertility impacts millions of people worldwide, and early identification of risk factors can support more timely counseling and intervention. A predictive model can help clinicians flag higher-risk patients and guide conversations around modifiable behaviors such as smoking and alcohol use.

## Data
- Source: UCI Machine Learning Repository – Fertility Diagnosis dataset
- Observations: 100 individuals
- Target: Fertility status (Normal vs. Altered)
- Features: Age, season, childhood diseases, accident/trauma, surgery, fever, smoking habits, alcohol, hours sitting, etc.

## Methods
- Language: R
- Libraries: `tidymodels`, `themis`, `xgboost`, `vip`
- Preprocessing: factor encoding, normalization, SMOTE-style oversampling for minority class
- Models:
  - Logistic Regression (baseline, interpretable)
  - Random Forest
  - XGBoost (tuned)
- Evaluation:
  - 5-fold cross-validation
  - Metrics: ROC AUC, F1 Score, Accuracy

## Key Results
- XGBoost achieved the strongest overall performance (AUC ≈ 0.90+).
- Smoking habit, alcohol consumption, and age emerged as the most influential predictors.
- Tree-based models capture non-linear relationships, while logistic regression provides a transparent baseline.

## Repository Structure
- `code/` – R scripts and/or R Markdown notebooks
- `data/` – (optional) data dictionary or instructions to obtain data
- `docs/` – project report, results & illustrations PDF
- `results/` – exported model outputs and plots

## How to Run
1. Open the R project or R script in the `code/` folder.
2. Install required packages:
   ```r
   install.packages(c("tidymodels", "themis", "xgboost", "vip"))

