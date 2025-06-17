# Insurance-Risk-and-Pricing-Analytics

## Overview
This project explores historical car insurance claims data for risk and marketing analytics in South Africa. The analysis focuses on exploratory data analysis (EDA), statistical modeling, and reproducible data workflows.

## Project Structure
- `data/` — Raw and processed datasets (tracked with DVC).
- `notebooks/` — Jupyter notebooks for EDA and analysis.
- `src/` — Source code for reusable functions.
- `.github/workflows/` — CI/CD configuration.

## Setup
1. Create a virtual environment and activate it.
2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
3. If using DVC:
   ```
   pip install dvc
   dvc pull
   ```

## Goals
- Summarize and visualize key insurance data features.
- Assess risk by geography, vehicle, and demographics.
- Set up reproducible, version-controlled analysis.

## Data Version Control (DVC)

This repo uses [DVC](https://dvc.org/) to track datasets and ensure data reproducibility.

### How to use

- To get data:  
  ```
  dvc pull
  ```
- To add new data:  
  ```
  dvc add data/insurance_claims.csv
  git add data/insurance_claims.csv.dvc
  git commit -m "Update data"
  dvc push
  ```
- DVC remote: `/absolute/path/to/your/local/storage`


# Task 3: A/B Hypothesis Testing Summary

### Objective:
To determine whether there are statistically significant differences in claim risk and profit margin across key customer and geographic segments.

---

## Hypotheses & Results

### H₀ 1: No risk difference across Provinces
- ✅ Rejected
- 📌 Provinces differ significantly in claim frequency, severity, and margin.
- 🔍 Gauteng showed notably higher claim risk — consider regional pricing adjustments.

---

### H₀ 2: No risk difference across Zip Codes
- ✅ Rejected (risk), ❌ Not rejected (margin)
- 📌 Some postal codes show significantly higher claim frequency and severity.
- 🔍 Consider zoning strategies to fine-tune premiums.

---

### H₀ 3: No risk difference by Gender
- ❌ Not rejected (p > 0.05 for all)
- 📌 No evidence that claim patterns differ between men and women.
- 🔍 Gender-based pricing is unnecessary and should be avoided.

---

## Business Recommendation

Focus premium adjustments on **location-based factors (province/postal code)** instead of personal factors like **gender**. This approach ensures a fair, risk-adjusted, and data-driven pricing model.


## Contributors
- EyasuGet

