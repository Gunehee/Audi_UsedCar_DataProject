# Audi_UsedCar_DataProject

# Audi Used Car Price Analysis & Prediction

**Author**: Josh  
**Date**: June 2025

---

## 📌 Project Overview

This project aims to analyze and predict the prices of used Audi vehicles using a combination of statistical methods and machine learning models. By examining factors such as model year, mileage, fuel type, transmission type, and engine size, the analysis uncovers key pricing determinants and translates them into deployable tools:

- **Market Price Lookup Service**: Returns the average and median resale value of a vehicle based on given attributes.
- **Price Prediction Service**: Provides a model-based suggested price and estimated error margin using trained regression models.

---

## 🔍 Key Features

- Log-transformed price modeling for normality and prediction accuracy.
- Statistical testing (t-tests, ANOVA) to confirm price differences by fuel type, transmission, year, and mileage.
- Multiple machine learning models including:
  - Linear Regression (R² ≈ 0.72)
  - Logistic Regression (Accuracy ≈ 78%)
  - Random Forest Classifier (Accuracy ≈ 80%)
- Clustering (Hierarchical & K-Means) + PCA for market segmentation.
- Service scripts for real-time price check and price prediction.

---

## 🧠 Methodology Summary

### Data Preprocessing
- Removed outliers based on boxplot thresholds.
- Handled missing values by imputation or labeling unknowns.
- Created derived variables: `log_price`, `year_G`, and `tax2`.

### Statistical Testing
- t-tests confirmed significant price differences across fuel types and transmissions.
- ANOVA + Tukey HSD validated mileage group and year group effects on price.

### Predictive Modeling
- **Linear Regression**: Explained ~72% of price variability; core predictors include year, mileage, engine size, and hybrid/auto indicators.
- **Classification**: Successfully categorized vehicle rating with 78–80% accuracy using logistic regression and random forest.

### Clustering & PCA
- Both Hierarchical and K-Means revealed 3 distinct clusters:
  - High-price, low-mileage, newer cars
  - Mid-price, mid-mileage, average models
  - Low-price, high-mileage, older cars
- PCA confirmed cluster separation using two principal components (explaining ~75% variance).

### Service Implementation
- **`price_lookup.py`**: Given input specs, returns market average & median prices.
- **`price_prediction.py`**: Uses trained regression to estimate a fair listing price and confidence bounds.

---




