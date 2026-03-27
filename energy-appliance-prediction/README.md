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
| Model             | MAE (Wh) | RMSE (Wh) | R2      |
|-------------------|----------|-----------|---------|
| Linear Regression | 26.33    | 57.36     | 0.5422  |
| CNN-LSTM          | 36.24    | 81.88     | 0.0671  |
| LSTM              | 47.87    | 82.44     | 0.0543  |
| GRU               | 48.92    | 93.70     | -0.2216 |
| Random Forest     | 62.65    | 92.14     | -0.1813 |

Best overall model: Linear Regression
Best deep learning model: CNN-LSTM (saved as models/trained_model.h5)
