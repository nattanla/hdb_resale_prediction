# HDB Resale Price Prediction (Python, ML)

## 📌 Problem Statement
Housing affordability is a major concern in Singapore, where resale HDB prices fluctuate based on multiple factors such as location, flat type, floor area, and lease duration
This project aims to predict HDB resale prices using machine learning models, helping to uncover which property features most influence pricing and improve forecasting accuracy

---

## Objectives
- Analyse and clean HDB resale transaction data for model readiness
- Identify key factors that influence housing prices
- Build and evaluate machine learning models (Linear Regression, XGBoost) to predict resale prices
- Compare model performance using **Mean Absolute Error (MAE) and Root Mean Square Error (RMSE) metrics

---

## Approach

1. **Data Cleaning & Exploration**
   - Handled missing values, duplication and outliers
   - Engineered new features to enhance predictive performance:
     - Derived a representative floor variable accounting for maximum floor height
     - Calculated the number of years left on the property lease
     - MRT 'Region' by categorising each location by proximity to MRT lines and grouping them by region
   - Conducted exploratory analysis to visualise feature distributions and identify correlations with resale price

2. **Feature Engineering**
   - Encoded categorical variables  
   - Selected relevant predictors using correlation and feature importance analysis

3. **Model Development**
   - Trained and tested Linear Regression and XGBoost models
   - Performed hyperparameter tuning to improve predictive accuracy
   - Evaluated both models using RMSE, and R² Score

4. **Insights & Interpretation**
   - Compared predicted vs. actual resale prices
   - Visualised residuals and model performance using Matplotlib and Seaborn

---

## Results
| Model | RMSE | R² Score |
|:------|:----|:---------|
| Linear Regression | ~70,990 | ~0.752 |
| XGBoost | ~38,748 | ~0.92 |

Key findings:
- **XGBoost** performed better in capturing non-linear relationships.  
- The analysis identified the top three factors that most significantly influence HDB resale prices:
  - Location (Central Region)
  - Flat Size
  - Proximity to Hawker Centres

---
