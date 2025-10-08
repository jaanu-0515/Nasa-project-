 🚀 Remaining Useful Life (RUL) Prediction — NASA Turbofan Engine Dataset

This project focuses on **predicting the Remaining Useful Life (RUL)** of aircraft engines using advanced **machine learning techniques** applied to the **NASA CMAPSS Turbofan Engine Degradation dataset**.

The goal is to estimate how long an engine can operate before failure by analyzing time-series data collected from multiple onboard sensors. Accurate RUL prediction helps in **preventive maintenance**, **cost reduction**, and **improving engine reliability**.

The dataset used in this project is sourced from **NASA’s CMAPSS simulation** and is publicly available on **Kaggle** — *NASA Turbofan Engine Degradation Simulation Data Set*.

The dataset was obtained from Kaggle — NASA Turbofan Engine Degradation Simulation Dataset


⚙️ Project Summary

Jet engines gradually degrade over time due to continuous exposure to high temperature, pressure, and operational stress. Predicting the Remaining Useful Life (RUL) of these engines is essential for ensuring reliability, safety, and cost efficiency.

This project aims to develop machine learning models capable of estimating the RUL, which represents the number of operational cycles left before engine failure occurs. Accurate RUL prediction supports the transition from reactive to predictive maintenance strategies, helping to identify potential issues before they lead to system breakdowns.

The implementation of RUL prediction provides several advantages. It enables timely maintenance actions to prevent unexpected failures, reduces downtime, and improves overall operational efficiency. In addition, it optimizes maintenance costs by allowing data-driven planning and resource allocation. Furthermore, by monitoring engine health and degradation patterns, the lifespan and performance of engines can be significantly extended.

🚀 Project Pipeline


1. Load the dataset (`train_FD001.csv`)
2. Preprocess and clean the data
3. Assign appropriate column names
4. Remove unwanted spaces and handle missing values
5. Compute Remaining Useful Life (RUL) for each engine
6. Apply feature scaling using **MinMaxScaler**
7. Split the data into training and testing sets
8. Train three regression models:

   * Linear Regression
   * Decision Tree Regressor
   * Random Forest Regressor
9. Predict RUL values for the test data
10. Evaluate model performance using:

    * Mean Squared Error (MSE)
    * Root Mean Squared Error (RMSE)
    * Coefficient of Determination (R²)
11. Compare model results and identify the best-performing algorithm


📊 Dataset Overview

The dataset used in this project is the NASA Turbofan Engine Degradation Simulation Data (FD001).
Each record corresponds to a specific engine cycle and contains operational settings, sensor readings, and computed RUL values.


| **Type**                 | **Description / Features**           |
| ------------------------ | ------------------------------------ |
| **Identification**       | `engine_id`, `cycle`                 |
| **Operating Conditions** | `Altitude`, `Mach`, `Throttle_Angle` |
| **Sensor Measurements**  | 21 condition-monitoring sensors      |
| **Target Variable**      | Remaining Useful Life (RUL)          |



| engine_id | cycle | total_temp_at_fan_inlet | ... | RUL |
| --------- | ----- | ----------------------- | --- | --- |
| 1         | 1     | 518.7                   | ... | 191 |
| 1         | 100   | 532.1                   | ... | 91  |
| 1         | 200   | 559.3                   | ... | 0   |


Evaluation Metrics


| **Model**                   | **RMSE ↓** | **MSE ↓** | **R² ↑** | **Remarks**                                |
| --------------------------- | ---------- | --------- | -------- | ------------------------------------------ |
| **Linear Regression**       | 44.30      | 1962.93   | 0.578    | Baseline model with moderate performance   |
| **Random Forest Regressor** | 41.29      | 1704.79   | 0.634    | Best-performing model with high accuracy   |
| **Decision Tree Regressor** | 61.52      | 3785.07   | 0.187    | Overfitting observed, lower generalization |
