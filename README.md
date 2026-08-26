# Mental Health ML Pipeline – StudentLife

A machine learning project for predicting **next-day mood** using behavioral and mental-health related features inspired by the StudentLife dataset.

## Project Overview

This project demonstrates an end-to-end machine learning pipeline including:

- Data preparation
- Data cleaning
- Feature engineering
- Model training
- Model evaluation
- Feature importance analysis
- Data visualization

> **Note:** The current project uses synthetic StudentLife-like data for demonstration and does not directly use the original StudentLife dataset.

## Dataset

The dataset contains:

- **48 users**
- **70 days per user**
- **3,360 records**
- Stress, mood, exercise, and walking features
- Simulated missing values

After preprocessing and feature engineering, the final dataset contains **3,264 records**.

## Features

The model uses:

- Stress
- Previous-day stress
- 3-day average stress
- Previous-day mood
- 3-day average mood
- Exercise
- Walking

### Target

**Next-day mood**

## Machine Learning Models

The following models are compared:

1. Mean Baseline
2. Linear Regression
3. Random Forest Regressor

## Results

| Model | RMSE | R² |
|---|---:|---:|
| Mean Baseline | 0.6233 | -0.0013 |
| Linear Regression | **0.5510** | **0.2177** |
| Random Forest | 0.5586 | 0.1958 |

### Best Model

**Linear Regression**

- RMSE: **0.5510**
- R²: **0.2177**
- RMSE improvement over baseline: **11.61%**

## Key Findings

- Previous mood and stress are useful for predicting next-day mood.
- Rolling 3-day averages help capture short-term trends.
- Mood and stress history were more useful than individual behavioral features in this experiment.
- Linear Regression performed slightly better than Random Forest.

## Technologies Used

```text
Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
Jupyter Notebook
Google Colab
