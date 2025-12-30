# RainML-daily--Reconstruction
Python-based multi-stage framework for daily rainfall time-series reconstruction in seasonal tropical forest ecosystems using unsupervised anomaly detection, bias-corrected reanalysis and satellite data, and multi-objective machine learning selection.

## Repository structure

- ML_daily.py  
  Main script for daily rainfall reconstruction using machine learning,
  including anomaly detection (Isolation Forest / LOF), bias correction
  via Quantile Mapping, feature engineering, and Pareto–Borda selection.

- ML_hourly_lstm.py  
  Script for hourly rainfall gap filling using a bidirectional LSTM
  architecture to capture short-term convective dynamics.

- ML_hourly_prophet.py  
  Diagnostic script using Prophet to analyze sub-daily and seasonal
  rainfall components (not intended as final imputation model).
