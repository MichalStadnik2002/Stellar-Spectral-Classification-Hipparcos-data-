# Stellar Spectral Classification (Hipparcos)

## Overview
This project applies machine learning methods to classify stellar spectral types using photometric data from the Hipparcos mission. The goal is to approximate spectroscopic information (spectral type) using features that are easier to obtain at scale.

## Motivation
Spectral classification typically requires spectroscopic observations, which are time-consuming and resource-intensive. In contrast, photometric measurements (magnitudes in different bands) are widely available for large numbers of stars. This project explores how well spectral types can be predicted from photometric features.

## Data
- Source: Hipparcos dataset (https://www.kaggle.com/datasets/konivat/hipparcos-star-catalog)
- Features:
  - Parallax (used to compute absolute magnitude)
  - Apparent magnitudes
  - Color indices
- Target:
  - Stellar spectral type

## Methods
- Data preprocessing:
  - Computation of absolute magnitude from parallax
  - Feature engineering (color indices)
  - Data cleaning
  - Handling class imbalance
- Models:
  - Decision Trees (Single decision tree, Random forest, ADABoost, XGBoost, CatBoost)
  - k-Nearest Neighbors
  - Multinomial Logistic Regression
  - Simple neural network
  

## Results
- Compared models using standard classification metrics (F1-score, confusion matrix)
- Best model: Single Decision Tree
- F1 score: 69.64%

## Conclusion
The results show that photometric features contain sufficient information to approximate stellar spectral types to a certain degree. This approach can be useful in large-scale surveys where spectroscopic data is unavailable. However, due to class imbalance the rare types of stars can be ommitted.

## Technologies
- Python
- NumPy, pandas
- scikit-learn
- matplotlib / seaborn

## Future Work
- Deal with class imbalance
- Incorporate measurement uncertainties
- Apply to larger datasets (e.g. Gaia)
