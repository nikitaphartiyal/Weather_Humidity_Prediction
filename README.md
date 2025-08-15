Linear Regression - Weather Humidity Prediction
📌 Overview

This project analyzes 96,453 hourly weather observations across 12 features, focusing on predicting humidity levels based on other weather parameters.
The dataset includes temperature, wind speed, pressure, and other meteorological measurements.

📊 Dataset Description

Rows: 96,453 hourly observations

Columns: 12 weather-related features

Key Features

Temporal: Formatted Date (timestamp)

Weather Conditions:

Summary (text description)

Precip Type (categorical: rain/snow/none)

Numerical Measurements:

Temperature (C)

Apparent Temperature (C)

Humidity (0–1 scale)

Wind Speed (km/h)

Wind Bearing (degrees)

Visibility (km)

Pressure (millibars)

Other:

Loud Cover (all zeros - potentially droppable)

Daily Summary (text description)

🛠 Data Preprocessing

Handled missing values in Precip Type (517 nulls)

Filled based on humidity and temperature conditions

Remaining nulls filled with mode value

Dropped irrelevant columns for modeling:

Formatted Date

Summary

Precip Type

Daily Summary

📈 Exploratory Data Analysis

Visualized distribution of weather summaries and precipitation types

Created pie charts for top daily summaries

Analyzed relationships between:

Temperature vs Humidity

Humidity vs Apparent Temperature

🤖 Modeling Approach

Target Variable: Humidity
Features Used:

Temperature (C)

Apparent Temperature (C)

Wind Speed (km/h)

Wind Bearing (degrees)

Visibility (km)

Loud Cover

Pressure (millibars)

Models Implemented & Performance
Model	MAE	MSE	R²
Linear Regression	0.11	0.02	0.47
Ridge Regression	0.11	0.02	0.47
Lasso Regression	0.15	0.03	0.13

Key Insight: Linear & Ridge Regression performed best with R² = 0.47, explaining ~47% of the variance in humidity.

🚀 How to Run
git:https://github.com/nikitaphartiyal/regression.git
Install dependencies

pip install numpy pandas matplotlib seaborn scikit-learn


Run the project

Jupyter Notebook:

jupyter notebook


Open the project .ipynb file and run all cells.

Python Script:

python main.py

📦 Dependencies

Python 3.x

NumPy

Pandas

Matplotlib

Seaborn

Scikit-learn

🔮 Future Work

Experiment with more complex models (Random Forest, XGBoost, etc.)

Apply time-series analysis

Engineer features from datetime components (month, season, etc.)

Perform hyperparameter tuning for improved performance
