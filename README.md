# Prediction-of-Vegetation-Indices
This project aims to predict future EVI values based on historical EVI patterns derived from satellite observations. Using machine learning regression techniques and Earth observation data, the project contributes to the early detection of areas at risk of vegetation loss.

> **End-to-end machine learning project** for satellite-based vegetation analysis and forecasting, showcasing data preprocessing, model comparison, evaluation, and future prediction using real-world remote sensing data.

## Project Overview

This project demonstrates an **end-to-end applied machine learning workflow** using real-world satellite data to analyze historical vegetation trends and forecast future vegetation conditions in **Malaysia**.

It focuses on:

* Translating raw remote sensing data into structured ML-ready datasets
* Comparing multiple machine learning models
* Evaluating model performance using standard regression metrics
* Generating interpretable forecasts to support environmental decision-making

The project highlights practical skills in **data preprocessing, model training, evaluation, forecasting, and visualization**, making it suitable for **data science and machine learning portfolios**.

---

## Objectives

* Analyze long-term vegetation dynamics in Malaysia using satellite-derived data.
* Design a reusable preprocessing pipeline for MODIS-based vegetation datasets.
* Train, compare, and evaluate multiple machine learning models.
* Forecast future EVI values and estimate green area coverage.
* Demonstrate applied machine learning skills on an environmental use case.

---

## Dataset

* **Source:** MODIS satellite products (e.g., MOD13 series for EVI, MCD12Q1 for land cover).
* **Study Area:** Malaysia
* **Time Period:** 2001–2024
* **Target Variable:** Enhanced Vegetation Index (EVI).

Due to cloud masking and sampling constraints, some spatial locations may be missing in certain years.

---

## Methodology

### 1. Data Preprocessing

* Data cleaning and handling of missing values.
* Temporal aggregation of pixel-level EVI values.
* Feature scaling and filtering based on pixel coverage thresholds.
* Preparation of time-series features for forecasting.

### 2. Machine Learning Models

Multiple models were evaluated, including:

* Linear Regression (baseline)
* Random Forest
* Support Vector Regression (SVR)
* **Gradient Boosting Tree (best-performing model)**

The Gradient Boosting Tree model demonstrated superior performance in capturing non-linear vegetation trends and temporal patterns.

### 3. Evaluation Metrics

* Mean Absolute Error (MAE)
* Mean Squared Error (MSE)
* R-squared (R²)

---

## Key Results

* Predicted mean EVI values for **2025–2029** remain stable at approximately **0.46**, indicating relatively stable vegetation conditions.
* Green area coverage was estimated using **EVI > 0.4** as the threshold.
* Predicted green coverage remains around **83%** across the forecast period.
* Forested regions consistently show higher EVI values, while urban and agricultural areas exhibit lower EVI.

These results suggest that Malaysia’s vegetation cover is expected to remain largely unchanged in the near future, with only minor fluctuations.

---

## Visualization

* Time-series plots of historical and predicted EVI values.
* Spatial maps comparing historical and forecasted EVI distributions.
* Green area coverage maps highlighting low-EVI regions that may require targeted intervention.

---

## Limitations

* Long-term forecasts rely on historical trends and may be less accurate.
* Climate variability and human activities were not explicitly modeled.
* The current model predicts EVI only and does not provide automated landcover-specific recommendations.
* Computational constraints limited extensive hyperparameter tuning for some models.

---

## Future Work

* Integrate climate and socio-economic variables as additional input features.
* Apply deep learning models (e.g., LSTM, GRU) for improved spatio-temporal forecasting.
* Train landcover classification models to automatically classify landcover types and integrate them into the EVI prediction pipeline.
* Generate landcover-specific vegetation management recommendations.
* Extend the framework to larger regions and longer time periods.
* Automate the pipeline for real-time or scenario-based monitoring.

---

## How to Run

### Option 1: Run with existing dataset (recommended)
1. Clone the repository:
```bash
git clone https://github.com/your-username/Prediction-of-Vegetation-Indices.git
cd Prediction-of-Vegetation-Indices
````

2. Install required dependencies:

```bash
pip install numpy pandas scikit-learn matplotlib
```

3. Open and run the notebook:

* Open `Machine Learning Assignment.ipynb` using Jupyter Notebook or Google Colab.
* **Skip the Google Earth Engine (GEE) integration section** unless you want to update or regenerate the dataset.
* Load the dataset directly from the provided CSV file and run the remaining cells sequentially.

### Option 2: Update dataset using Google Earth Engine (optional)

* Authenticate and enable Google Earth Engine.
* Run the GEE data extraction section in the notebook.
* Export the updated dataset and replace the existing CSV file.
* Re-run the remaining notebook cells.

---

## Technologies Used

* Python
* NumPy, Pandas
* Scikit-learn
* Matplotlib
* Google Earth Engine / MODIS data (data source)

---

## Conclusion

This project demonstrates how machine learning can be effectively applied to **real-world environmental and geospatial data**. It showcases the full ML lifecycle—from raw data preparation to model evaluation and future forecasting—using a meaningful sustainability-focused problem domain.

The work highlights practical strengths in **feature engineering, model selection, evaluation, and result interpretation**, making it well-suited as a **portfolio project for data science, machine learning, or environmental analytics roles**.
