# Audi_UsedCar_DataProject

## Audi Used Car Price Analysis & Prediction

**Author**: GunHee(Joshua) Lee  
**Date**: June 2025

---

## Project Overview

This project aims to analyze and predict the prices of used Audi vehicles using a combination of statistical methods and machine learning models. By examining factors such as model year, mileage, fuel type, transmission type, and engine size, the analysis uncovers key pricing determinants and translates them into deployable tools:

- **Market Price Lookup Service**: Returns the average and median resale value of a vehicle based on given attributes.
- **Price Prediction Service**: Provides a model-based suggested price and estimated error margin using trained regression models.

---

## Key Features

- Log-transformed price modeling for normality and prediction accuracy.
- Statistical testing (t-tests, ANOVA) to confirm price differences by fuel type, transmission, year, and mileage.
- Multiple machine learning models including:
  - Linear Regression (R² ≈ 0.72)
  - Logistic Regression (Accuracy ≈ 78%)
  - Random Forest Classifier (Accuracy ≈ 80%)
- Clustering (Hierarchical & K-Means) + PCA for market segmentation.
- Service scripts for real-time price check and price prediction.

---

## Methodology Summary

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
## Conclusion
This project delivers a full-cycle data science pipeline—from data preprocessing and statistical testing to machine learning modeling and service deployment—targeted at solving a practical, real-world problem: estimating the fair market price of used Audi vehicles. Through detailed analysis of over 6,000 listings, we identified key price-driving factors such as vehicle year, mileage, fuel type, and transmission type, and quantified their impact using both statistical inference and predictive models.

Not only did the regression model achieve strong performance (R² ≈ 0.72, RMSE ≈ 0.28 in log scale), but the integration of clustering and PCA also revealed consistent market segments. Furthermore, the development of two user-facing services—the Market Price Lookup and Price Prediction scripts—translates analytical findings into accessible, actionable tools. These scripts enable consumers, sellers, and platform operators to make better pricing decisions using objective data-driven benchmarks.

This project not only demonstrates technical competency in statistics, machine learning, and Python scripting, but also showcases the ability to transform analytical insights into tools with tangible business value. Future enhancements such as geolocation-aware pricing, vehicle option analysis, and a full-stack web dashboard can further evolve this project into a deployable B2C or B2B automotive pricing solution.

## Why This Project Matters

Buying or selling a used car is often clouded by uncertainty—what is a "fair" price? How do mileage, year, or fuel type really affect resale value? While dealers rely on experience, private sellers and buyers often lack access to objective, data-backed benchmarks.

This project was designed to close that gap. By analyzing thousands of real used Audi listings, we set out to uncover the data-driven logic behind used car pricing. The goal was twofold:

1. **Understand the market** through statistical analysis and visual exploration  
2. **Build tools** that could predict prices based on real-world vehicle attributes  

This isn't just a data analysis project—it's a practical solution built with industry applications in mind. It’s designed to assist:
- **Sellers**, who want to set competitive, yet profitable listing prices  
- **Buyers**, who want to avoid overpaying  
- **Online platforms**, looking to recommend accurate prices or identify anomalies




