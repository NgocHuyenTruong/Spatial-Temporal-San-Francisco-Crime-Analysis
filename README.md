# Advanced Analytics: Spatial and Temporal Crime Analysis in San Francisco

This repository contains a comprehensive spatial and temporal analysis of crime incidents in San Francisco from July to December 2012. The analysis focuses on four major crime categories: **Vandalism**, **Vehicle Theft**, **Robbery**, and **Drug/Narcotic offenses**, leveraging techniques such as exploratory data analysis, time series forecasting, spatial clustering, and predictive modeling.

---

## Objectives

- Identify crime **hotspots**
- Analyze **temporal patterns** and trends
- Forecast crime using **time series models**
- Detect **spatial clusters** and correlations
- Build predictive models to classify crime types based on location and time

---

## Dataset

- **Source:** [GeoDa Data and Lab](https://geodacenter.github.io/data-and-lab/)
- **Timeframe:** July 1, 2012 – December 31, 2012
- **Data Format:** Shapefiles (.shp) for each crime category
- **Total Records:** 13,472 (reduced to 10,153 after cleaning)

---

## Tools & Technologies

- **Programming Language:** Python
- **Libraries:**
  - `pandas`, `numpy` for data manipulation
  - `matplotlib`, `seaborn` for visualizations
  - `scikit-learn` for machine learning
  - `geopandas`, `libpysal`, `folium` for spatial analysis
  - `statsmodels`, `prophet` for time series forecasting

---

## Methodology

### 1. Data Preprocessing
- Merged shapefiles into a single GeoDataFrame
- Removed duplicate and redundant entries
- Converted coordinate systems (EPSG:2227 ➝ EPSG:4326)

### 2. Exploratory Data Analysis (EDA)
- Summary statistics and visualizations
- Crime distribution by type, time, and neighborhood

### 3. Time Series Analysis
- Daily, weekly, and monthly crime trends
- Anomaly detection using Z-scores
- Forecasting using ARIMA, Holt-Winters, and Prophet

### 4. Spatial Analysis
- Heatmaps and choropleth mapping
- Spatial clustering (K-Means, Hierarchical)
- Spatial lag analysis and spatial weights matrix

### 5. Predictive Modeling
- Feature engineering (e.g., Day of week, Block ID)
- Classification model to predict crime type

---

## Results & Insights

- **High Prevalence of Vandalism Incidents**: Vandalism emerged as the most frequent crime category (3,897 cases), followed by Vehicle Theft and Robbery. Most cases (8,018) had no resolution, while “Arrest, Booked” (1,682) was the most common actionable outcome.

- **Temporal Patterns with Distinct Peaks**: Crime incidents peaked mid-October and dipped on December 25, 2012. Fridays had the highest frequency, and October was the month with the most crime, hinting at possible event-driven influences.

- **ARIMA as the Best Forecasting Model**: ARIMA outperformed Holt-Winters and Prophet, achieving the lowest RMSE (11.05) and MAPE (20.95%) for short-term and seasonal trend forecasting.

- **Spatial Clustering in the Southern District**: The Southern police district had the highest crime concentration (2,006 cases). Drug/Narcotic and Robbery incidents clustered in the central-east area, while Vehicle Theft showed a wider distribution.

- **Predictive Power of Spatial and Temporal Features**: The LightGBM classifier achieved the highest accuracy (0.4653) in predicting crime categories. Longitude, latitude, and day of the week were the most informative features.

---

## Future Work

- Include more recent datasets for trend validation
- Apply deep learning models for better predictions
- Integrate external datasets (e.g., weather, local events)

---

## Getting Started

To run this project:

1. Clone the repository: [https://github.com/NgocHuyenTruong/Spatial-Temporal-San-Francisco-Crime-Analysis](https://github.com/NgocHuyenTruong/Spatial-Temporal-San-Francisco-Crime-Analysis)
2. Open the Jupyter Notebook for data analysis and model development.
3. Open the final report (`San_Francisco_Crime_Analysis_Report.pdf`) for a detailed summary of findings, methodology, and visualizations.

---

## Acknowledgments

- I would like to acknowledge the collaborative efforts of my team members, **Ngoc Anh Nguyen** and **Thanh Dung Nguyen**, in completing this project.
- GeoDa Center for Spatial Data Science
- Python open-source community
