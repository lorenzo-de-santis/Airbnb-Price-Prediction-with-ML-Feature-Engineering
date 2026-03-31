# Airbnb Price Prediction with Machine Learning

## Overview

This project focuses on predicting Airbnb listing prices (log-transformed) using machine learning models and feature engineering.

The analysis distinguishes between:

* **Hard features** (immutable property characteristics)
* **Soft features** (host behavior and listing attributes)
## Dataset

Available on Kaggle:
https://www.kaggle.com/datasets/lovishbansal123/airbnb-data 


## Approach

* Target: log(price)
* Models:

  * Linear Regression (baseline)
  * Gradient Boosting Machine (GBM)
* Data segmented by city for localized modeling

## Key Results

* Linear Regression (hard features) → baseline performance

* GBM (hard features) → improved predictive accuracy

* GBM (hard + soft features) → **best performance (R² ≈ 0.75 across cities)**

* Soft features significantly improve prediction, especially in competitive markets

* Non-linear models outperform linear models by capturing feature interactions

## Feature Engineering
* Missing values handled using KNN imputation based on feature similarity, including proximity in log price space, to preserve underlying data structure

* Hard features:
  accommodates · bedrooms · beds · reviews · distance from city center

* Soft features:
  property type · room type · cancellation policy · host behavior · amenities

## Explainability (SHAP)

* SHAP values used to:

  * identify feature importance
  * analyze city-specific drivers
* Key drivers:

  * room type (strongest)
  * distance from center
  * host behavior features

## Additional Analysis

* Text processing on descriptions & amenities
* No significant improvement in predictive performance

## Business Insights

* Location and property size are primary price drivers
* Host behavior (response rate, policies) impacts pricing in competitive markets
* Pricing strategies should be city-specific

## Tech Stack

KNIME · Gradient Boosting · Linear Regression · SHAP · Feature Engineering
