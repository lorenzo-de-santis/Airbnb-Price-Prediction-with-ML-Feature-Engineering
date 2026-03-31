# Airbnb Price Prediction with Machine Learning

## Overview

This project focuses on predicting Airbnb listing prices (log-transformed) using machine learning models and feature engineering.

## Key Contributions

* Feature engineering with **hard** (immutable property characteristics) and **soft** (host behavior and listing attributes) features
* KNN-based imputation for missing values
* Comparison of linear and non-linear models
* SHAP-based model interpretability

## Dataset

Available on Kaggle:
https://www.kaggle.com/datasets/lovishbansal123/airbnb-data 

## Results

* Linear Regression (hard features) → baseline

* Gradient Boosting (hard features) → improved performance

* Gradient Boosting (hard + soft features) → **best model (R² ≈ 0.75)**

* Key drivers:

  * room type
  * distance from city center
  * host behavior features

## Models

* Linear Regression
* Gradient Boosting Machine

## Structure

* `workflow_Airbnb.knwf` → KNIME workflow
* `Presentation.pdf` → analysis and results

## Tech Stack

KNIME · Machine Learning · SHAP · Feature Engineering
