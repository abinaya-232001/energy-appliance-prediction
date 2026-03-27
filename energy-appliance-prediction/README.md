# Appliance Energy Prediction Using Deep Learning

## Overview
Predicts household appliance energy consumption using multivariate time-series
deep learning models (LSTM, GRU, CNN-LSTM) on the Appliance Energy Prediction Dataset.

## Dataset
- 19,735 records at 10-minute intervals (January to May 2016)
- Target: Appliances energy consumption in Wh

## Setup
pip install -r requirements.txt

## Run
Open notebooks/EDA.ipynb and run all cells in order.

## Results
| Model             | MAE (Wh) | RMSE (Wh) | R2     |
|-------------------|----------|-----------|--------|
| Linear Regression | 26.45    | 57.39     | 0.5465 |
| GRU               | 34.62    | 70.11     | 0.3231 |
| CNN-LSTM          | 35.53    | 73.13     | 0.2636 |
| LSTM              | 40.62    | 78.00     | 0.1621 |
| Random Forest     | 63.74    | 92.91     | -0.1886|

Best deep learning model: GRU (saved as models/trained_model.keras)
