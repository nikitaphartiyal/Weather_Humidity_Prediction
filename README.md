# linear-regression-
Overview---
This project analyzes a dataset of 96,453 hourly weather observations with 12 features, focusing on predicting humidity levels based on other weather parameters. The dataset includes various weather measurements like temperature, wind speed, pressure, and more.

Dataset Description--
Rows: 96,453 hourly weather observations

Columns: 12 weather-related features

Key Features:
Temporal: Formatted Date (timestamp)

Weather Conditions:

Summary (text description)

Precip Type (categorical: rain/snow/none)

Numerical Measurements:

Temperature (C)

Apparent Temperature (C)

Humidity (0-1 scale)

Wind Speed (km/h)

Wind Bearing (degrees)

Visibility (km)

Pressure (millibars)

Other:

Loud Cover (all zeros - potentially droppable)

Daily Summary (text description)

Data Preprocessing--
Handled missing values in 'Precip Type' column (517 null values)

Replaced nulls based on humidity and temperature conditions

Filled remaining nulls with the mode (most frequent value)

Dropped irrelevant columns for modeling:

Formatted Date

Summary--

Precip Type

Daily Summary

Exploratory Data Analysis
Visualized distribution of weather summaries and precipitation types

Created pie charts for top daily summaries

Analyzed relationships between:

Temperature and Humidity

Humidity and Apparent Temperature

Modeling Approach
Target Variable: Humidity

Features Used:

Temperature (C)

Apparent Temperature (C)

Wind Speed (km/h)

Wind Bearing (degrees)

Visibility (km)

Loud Cover

Pressure (millibars)

Models Implemented:--
Linear Regression

MAE: 0.11

MSE: 0.02

R²: 0.47

Ridge Regression

MAE: 0.11

MSE: 0.02

R²: 0.47

Lasso Regression

MAE: 0.15

MSE: 0.03

R²: 0.13

Results--
Linear and Ridge Regression performed similarly with R² of 0.47

Lasso Regression had lower performance (R² of 0.13)

The best model can explain about 47% of variance in humidity levels

How to Run
Clone the repository

Install required packages:

text
pip install numpy pandas matplotlib seaborn scikit-learn
Run the Jupyter notebook or Python script

Dependencies
Python 3.x

NumPy

Pandas

Matplotlib

Seaborn

Scikit-learn

Future Work
Experiment with more complex models

Include time-series analysis

Feature engineering with datetime features

Hyperparameter tuning for better performance
