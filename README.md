# Electricity-Demand-Forecast

📊 **Delhi Electricity Load Forecasting Using Machine Learning**

🧠 “Predicting the future of power—one model at a time.”

---

## 🚀 Overview

This project presents a data-driven approach to forecasting total electricity demand (in MW) in Delhi by utilizing historical energy data along with past weather conditions. Three machine learning models—**Linear Regression**, **Random Forest Regressor**, and **XGBoost**—are used to compare performance and understand the impact of various features.

---

## 📌 Dataset Description

- **Source:** Real-world dataset (CSV)
- **Date Range:** 2018–2023

### 🧾 Columns Included

- **Weather Features:**  
  - Temperature (`temp2(c)`)
  - Wind Speed (`wind_speed50_ave`)
  - Precipitation (`prectotcorr`)
  - Surface Pressure (if available)

- **Energy Features:**  
  - Total Demand (MW) (`total_demand(mw)`)
  - Maximum Generation (MW) (`max_generation(mw)`)

- **Time Features:**  
  - Day, Month, Year

#### Sample Data

| temp2(c) | wind_speed50_ave | prectotcorr | total_demand(mw) | max_generation(mw) |
|----------|------------------|-------------|------------------|--------------------|
| 19.11    | 2.64             | 0.00        | 8000.0           | 7651.0             |

---

## 🛠️ Tools & Libraries

- **Programming Language:** Python
- **Data Manipulation:** Pandas, NumPy
- **Machine Learning:** scikit-learn (Linear Regression, Random Forest Regressor, Metrics)
- **Visualization:** Matplotlib, Seaborn
- **Development Environment:** Jupyter Notebook

---

## 🧪 ML Models Applied

### 📈 Linear Regression

- **Performance Metrics:**
  - **Train R²:** 0.896
  - **Test R²:** 0.901

### 🌳 Random Forest Regressor (Depth = 2)

- **Remarks:** Deliberately shallow depth limits its ability to capture non-linear interactions — underfits relative to the other two models
- **Performance Metrics:**
  - **Train R²:** 0.839
  - **Test R²:** 0.839

### 🚀 XGBoost Regressor

- **Params:** `n_estimators=200, max_depth=4, learning_rate=0.08, subsample=0.9, colsample_bytree=0.9`
- **Remarks:** Best performer — captures non-linear interactions between weather and time features without underfitting
- **Performance Metrics:**
  - **Train R²:** 0.987
  - **Test R²:** 0.941

---

## 📊 Model Comparison

| Model                | Train R² | Test R² | Train MSE | Test MSE |
|----------------------|----------|---------|-----------|----------|
| **Linear Regression**| 0.897    | 0.901   | 292,897   | 263,111  |
| **Random Forest**    | 0.839    | 0.839   | 455,537   | 427,145  |
| **XGBoost**           | 0.987    | 0.941   | 38,321    | 157,357  |

**Insight:** XGBoost achieves the best test performance, capturing non-linear interactions between weather and time features that Linear Regression misses, without underfitting the way the depth-limited Random Forest does. The gap between its train R² (0.987) and test R² (0.941) is worth watching — it's a healthy fit, not a red flag, but tighter regularization (lower `max_depth` or fewer estimators) could close that gap further if generalization becomes a priority over raw test score.

---

## 📉 Visualizations

1. **Actual vs. Predicted – Test Set**
2. **Residual Distribution**
3. **Feature Importance** (Based on Linear Regression coefficients)

---

## ✅ What I Learned

- **Data Preprocessing:** Cleaning, preprocessing, and managing date formats with Pandas.
- **Model Building:** Training and evaluating regression models.
- **Metrics Interpretation:** Understanding R², MSE, and the tuning of model parameters.
- **Visualization:** Presenting insights with clear and effective visuals.

---

## 🔮 Future Improvements

- **Hyperparameter Tuning:** Implement GridSearchCV/Optuna for more rigorous tuning of the XGBoost parameters used here.
- **Additional Regressors:** Explore Lasso, Ridge, and LightGBM for comparison.
- **Time-Series Analysis:** Incorporate time-series forecasting methods (ARIMA, LSTM).
