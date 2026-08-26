Mental Health ML Pipeline – StudentLife

A machine learning pipeline for predicting next-day mood using behavioral and mental-state features inspired by the StudentLife dataset.

Overview

This project demonstrates an end-to-end ML workflow for student mental-health trend analysis:

Data generation and preparation

Data cleaning and missing-value handling

Feature engineering

Next-day mood prediction

Model training and evaluation

Feature importance analysis

Visualization of results

Note: The current notebook uses synthetic StudentLife-like data for demonstration. It does not use the original StudentLife dataset directly.

Dataset

The notebook generates:

48 users

70 days per user

3,360 raw records

Features: stress, mood, exercise, and walk

Missing values are intentionally introduced to simulate real-world data

After preprocessing and target creation, the final modeling dataset contains 3,264 records.

Feature Engineering

The model uses 7 features:

stress

prev_stress

stress_3day_avg

prev_mood

mood_3day_avg

exercise

walk

The target is next-day mood.

Models

The project compares:

Mean Baseline

Linear Regression

Random Forest Regressor

Results

Model

RMSE

R²

Baseline

0.6233

-0.0013

Linear Regression

0.5510

0.2177

Random Forest

0.5586

0.1958

Best model: Linear Regression

It achieved an 11.61% reduction in RMSE compared with the baseline.

Key Findings

mood_3day_avg and stress_3day_avg are among the most important predictive features.

Previous mood and stress values provide useful temporal information.

Rolling averages help capture short-term trends in mood and stress.

Behavioral features such as exercise and walking are included as potential indicators of mental well-being.

Visualizations

The notebook generates visualizations for:

Linear Regression feature importance

Random Forest feature importance

Predicted vs. actual mood

Model performance comparison

Stress and mood trends over time

Technologies

Python

Pandas

NumPy

Matplotlib

Seaborn

Scikit-learn

Jupyter Notebook / Google Colab

How to Run

Clone the repository

git clone https://github.com/Bharadwaj1433/Mental_Health_ML_Pipeline_StudentLife.git
cd Mental_Health_ML_Pipeline_StudentLife

Run the notebook

Open:

Mental_Health_ML_Pipeline_StudentLife.ipynb

The notebook can be run using Jupyter Notebook or Google Colab.

Project Structure

Mental_Health_ML_Pipeline_StudentLife/
│
├── Mental_Health_ML_Pipeline_StudentLife.ipynb
└── README.md

Limitations

This is a demonstration project using synthetic data. The results should not be interpreted as clinical predictions or medical advice.

Author

Bharadwaj Rachakonda

GitHub: Bharadwaj1433
