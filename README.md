# Electricity-Demand-Forecast

📊 **Delhi Electricity Load Forecasting Using Machine Learning**

🧠 “Predicting the future of power—one model at a time.”

---

## 🚀 Overview

This project presents a data-driven approach to forecasting total electricity demand (in MW) in Delhi by utilizing historical energy data along with past weather conditions. Two machine learning models—**Linear Regression** and **Random Forest Regressor**—are used to compare performance and understand the impact of various features.

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

- **Remarks:** Captures non-linear interactions
- **Performance Metrics:**
  - **Train R²:** 0.839
  - **Test R²:** 0.839

---

## 📊 Model Comparison

| Model                | Train R² | Test R² | Train MSE | Test MSE |
|----------------------|----------|---------|-----------|----------|
| **Linear Regression**| 0.896    | 0.901   | 292,897   | 263,111  |
| **Random Forest**    | 0.839    | 0.839   | 455,537   | 427,145  |

**Insight:** Despite its simplicity, the Linear Regression model outperformed the Random Forest model on this dataset.

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

- **Hyperparameter Tuning:** Implement GridSearchCV for optimal model parameters.
- **Additional Regressors:** Explore other models like XGBoost, Lasso, and Ridge.
- **Time-Series Analysis:** Incorporate time-series forecasting methods (ARIMA, LSTM).

