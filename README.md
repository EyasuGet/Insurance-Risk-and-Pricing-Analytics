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

## Contributors
- EyasuGet

