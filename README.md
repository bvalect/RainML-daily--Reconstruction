# RainML-daily--Reconstruction

Python-based multi-stage framework for daily rainfall time-series reconstruction in seasonal tropical forest ecosystems using unsupervised anomaly detection, bias-corrected reanalysis and satellite data, and multi-objective machine learning selection.

This repository accompanies the manuscript:
**“Machine Learning–Based Methodology for Rainfall Data Reconstruction in Seasonal Forest Ecosystems”**.

---

## Overview

Reliable rainfall records are essential for hydrological and ecohydrological studies, yet long observational series in tropical regions are frequently affected by gaps and instrumental inconsistencies.  
This repository provides the research code used to reconstruct daily and hourly precipitation series through a multi-stage workflow that prioritizes hydrological realism over pure statistical error minimization.

The framework integrates:
- Unsupervised anomaly detection (Isolation Forest, Local Outlier Factor),
- Bias correction of reanalysis and satellite products via Quantile Mapping,
- Feature engineering capturing temporal memory and seasonality,
- Machine learning models for gap filling,
- Multi-objective model selection based on RMSE and Kling–Gupta Efficiency (KGE).

---

## Repository structure

- **ML_daily.py**  
  Main script for daily rainfall reconstruction using machine learning models (e.g., Random Forest, XGBoost, CatBoost, SARIMA).  
  Includes anomaly detection, bias correction, feature engineering, and Pareto–Borda model selection.

- **ML_hourly_lstm.py**  
  Script for hourly rainfall gap filling using a bidirectional LSTM architecture designed to capture short-term convective dynamics.

- **ML_hourly_prophet.py**  
  Diagnostic script using Prophet to analyze sub-daily and seasonal rainfall components.  
  This script is intended for exploratory and diagnostic analysis and not as the final imputation model.

---

## Data availability

Observed rainfall data used in this study are subject to institutional restrictions and are not included in this repository.

Publicly available datasets used as exogenous predictors include:
- ERA5 and ERA5-Land reanalysis (ECMWF),
- CHIRPS v2.0,
- PERSIANN-CDR.

Users must provide their own data files following the formats described in the scripts.

---

## Software requirements

- Python ≥ 3.10  
- Core libraries: numpy, pandas, scikit-learn, xgboost, catboost, optuna, shap, statsmodels, prophet, tensorflow/keras, matplotlib, seaborn

---

## Reproducibility

The complete computational workflow, model configurations, and validation strategy are described in detail in the associated manuscript.  
This repository is intended to ensure methodological transparency and reproducibility of the results.

---

## License

This project is licensed under the MIT License.
