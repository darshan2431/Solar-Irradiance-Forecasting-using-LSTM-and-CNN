# Solar Irradiance Forecasting using LSTM and CNN

Hourly Global Horizontal Irradiance (GHI) forecasting using deep learning models trained on NASA MERRA-2 meteorological data.

## Overview
This project replicates and extends the methodology from a peer-reviewed IEEE paper on solar irradiance forecasting. The original paper used the NREL Los Angeles dataset; this implementation uses the **NASA MERRA-2 dataset** as an alternative data source, validating the approach across a different geographic and meteorological context.

## Models Implemented
- **Stacked LSTM** — 3 descending layers (32/16/8 units), 72-hour lookback window
- **1D CNN** — 32 filters, kernel size 3, no max pooling
- **ML Baselines** — Linear Regression, Decision Tree, Random Forest, XGBoost, LightGBM

## Dataset
- **Source:** NASA MERRA-2 (Modern-Era Retrospective Analysis for Research and Applications)
- **Features:** GHI, Temperature, Humidity, Wind Speed, Pressure, Clearness Index
- **Preprocessing:** Min-Max normalization, linear interpolation for missing values, 72-hour sliding window

## Results
Models evaluated using RMSE, MAE, MAPE, and Pearson Correlation Coefficient (r).

## Tech Stack
Python, TensorFlow/Keras, Scikit-learn, XGBoost, LightGBM, Pandas, NumPy, Matplotlib, Seaborn

## Reference
Bouadjila et al., "Hourly Solar Irradiance Forecasting Using Long Short Term Memory and Convolutional Neural Networks", Smart Grids and Sustainable Energy, 2024.
