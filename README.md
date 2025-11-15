# Energy Consumption Forecasting and Multi-Target Regression
## Overview

This repository showcases a machine learning project focused on **predicting building energy consumption** based on diverse input features, including structural, occupancy, and environmental factors. The solution implements a **multi-target regression** approach using an exploratory dual-model architecture to predict two interdependent outcomes: **Energy Consumption** and **Number of Occupants**.

This work demonstrates proficiency in the end-to-end machine learning pipeline, from data preparation and feature engineering to model training and performance evaluation, making it a valuable asset for ML/AI roles.

## Key Skills and Techniques Demonstrated

* **Multi-Output Regression:** Successfully trained Linear Regression models to predict multiple target variables (`Energy Consumption` and `Number of Occupants`) simultaneously.
* **Data Preprocessing:** Handled categorical variables (`Building Type`, `Day of Week`) using `LabelEncoder` for feature preparation.
* **Feature Subset Analysis:** Explored the impact of different feature groups by training two separate Linear Regression models:
    * **Model A:** Trained exclusively on structural features (`Building Type`, `Square Footage`).
    * **Model B:** Trained on environmental/usage features (`Appliances Used`, `Average Temperature`, `Day of Week`).
* **Model Evaluation:** Rigorous assessment performed using key regression metrics: **R-squared ($R^2$)**, **Mean Absolute Error (MAE)**, and **Mean Absolute Percentage Error (MAPE)**.
* **Core Libraries:** Pandas, Scikit-learn (`sklearn`).

## Results Summary

The dual Linear Regression models successfully captured significant variance in the multi-target prediction task. Model A (Structural Features) demonstrated a particularly strong fit for the overall dataset.

| Model | Primary Features | R² Score | Mean Absolute Error (MAE) |
| :--- | :--- | :--- | :--- |
| **Model A** | Building Type, Square Footage | $\approx$ 0.783 | $\approx$ 305.6 |
| **Model B** | Appliances Used, Avg. Temp, Day of Week | $\approx$ 0.672 | $\approx$ 407.9 |

The average Mean Absolute Percentage Error (MAPE) was also calculated to assess prediction accuracy in relative terms.

## Repository Contents

* `TrainingModels.ipynb`: The Jupyter notebook containing the full project workflow, including data loading, preprocessing, model training, and metric calculation.
* `data/`: Directory for the source dataset (e.g., `train_energy_data.csv`).
