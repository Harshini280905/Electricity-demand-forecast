# Electricity-demand-forecast
📊 Delhi Electricity Load Forecasting Using Machine Learning

🧠 “Predicting the future of power—one model at a time.”

🚀 My First ML Project | Built with Linear Regression & Random Forest | Forecasting electricity demand in Delhi using real-world weather + energy data.

📌 Overview:

This project is a data-driven approach to forecasting total electricity demand (in MW) in Delhi using past weather conditions and historical generation data.

I used both Linear Regression and Random Forest Regressor to compare performance and understand feature contributions.

🗃️ Dataset Description:

✅ Source: Real-world dataset (CSV)

🗓️ Date Range: 2018–2023

🧾 Columns:

Weather features: temperature, wind speed, precipitation, surface pressure

Energy features: total demand, max generation

Time features: day, month, year
Sample:

| temp2(c) | wind_speed50_ave | prectotcorr | total_demand(mw) | max_generation(mw) |
|----------|------------------|-------------|-------------------|---------------------|
| 19.11    | 2.64             | 0.00        | 8000.0            | 7651.0              |


🛠️ Tools & Libraries:

Python (Pandas, NumPy)

scikit-learn (Linear Regression, Random Forest, Metrics)

Matplotlib, Seaborn for visualization

Jupyter Notebook


🧪 ML Models Applied:

📈 Linear Regression


Achieved:

Train R²: 0.896

Test R²: 0.901

🌳 Random Forest Regressor (Depth=2)

Captures non-linear interactions

Achieved:

Train R²: 0.839

Test R²: 0.839

📊 Model Comparison

Model	Train R²	Test R²	Train MSE	Test MSE
Linear Regression	0.896	0.901	292,897	263,111
Random Forest	0.839	0.839	455,537	427,145

📌 Insight: Despite its simplicity, Linear Regression outperformed Random Forest for this dataset.


📉 Visualizations:

1️⃣ Actual vs Predicted – Test Set

2️⃣ Residual Distribution

3️⃣ Feature Importance (Linear Regression Coefficients)

✅ What I Learned

🧹 Data cleaning, preprocessing, and date handling with Pandas

⚙️ Building, training, and evaluating regression models

📈 Interpreting model metrics and tuning parameters

🎨 Presenting insights with clear visuals


🔮 Future Improvements:

Add hyperparameter tuning (GridSearchCV)

Explore other regressors: XGBoost, Lasso, Ridge

Add time-series analysis (ARIMA, LSTM)

