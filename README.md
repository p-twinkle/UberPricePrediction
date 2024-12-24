# Uber Price Prediction Project

## Overview

This project aims to understand Uber's pricing strategy to help a cab service startup offer more cost-effective rides. The analysis involves implementing various machine learning models to predict Uber ride prices based on different features.

## Data Understanding and Preprocessing

- Dropped NULL values and duplicates
- Renamed, split, and selected columns, including typecasting
- Detected and treated anomalies in data (e.g., abnormal latitude/longitude values)

## Feature Engineering

### Time-based Features
- Pickup time of day (categorized as Morning, Afternoon, Evening & Night)
- Weekday flag (weekday or weekend)
- Holiday flag

### Location-based Features
- MAP route distance (using Google API)
- Zip codes (using reverse geocoding)

### Miscellaneous Features
- UberXL flag (based on passenger count)

## Models Implemented

1. Multiple Linear Regression
2. Stepwise Selection
3. Single Regression Tree
4. Random Forest/Bagging
5. Boosting (XGBoost / GBM)
6. BART (Bayesian Additive Regression Trees)

## Model Comparison

| Model | Training RMSE | Test RMSE | Strengths | Weaknesses |
|-------|---------------|-----------|-----------|------------|
| Linear Regression / Best Subset | 4.722069 | 4.725299 | Captures categorical variable effects better | High error value, MSE doesn't reduce with multiple variables |
| Single Regression Tree | - | - | - | Overfitting, predictions not much better than linear |
| Random Forest/Bagging | 4.276331 | 4.436574 | Low RMSE, better for complex relationships | Overfitting, computationally intensive |
| Boosting (XGBoost / GBM) | 3.920847 | 4.374432 | Regularization reduces overfitting, parallel processing, best RMSE | Harder to interpret |

## Key Findings

- The distance driven by the Uber is the most important predictor of price
- Random Forests (Boosting) performs best based on RMSE
- Linear Regression remains the most interpretable model

## Challenges and Future Work

- Improve location features (zip code, county, area code)
- Increase the number of data points
- Obtain distributed data points from multiple states
- Consider SEC classification

## Usage

1. Clone the repository
2. Install required dependencies
3. Run the Jupyter notebooks in the following order:
   - Data_Preprocessing.ipynb
   - Feature_Engineering.ipynb
   - Model_Implementation.ipynb
   - Model_Comparison.ipynb

## Contributors

- Albert
- Twinkle
- Sarthak
- Gaurav 
