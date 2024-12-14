# Predicting Aircraft Noise Exceedances in the San Francisco Bay Area

## INDENG242A Final Project
### Team Members:
- **Mitchell Wu**
- **Yunpu Zhao**
- **Wencong Wang**
- **Yingyu Zhu**
- **Zixuan Li**

---

## Project Overview

Aircraft noise pollution significantly impacts the quality of life for communities surrounding airports. This project aims to analyze noise exceedance events recorded near **San Francisco International Airport (SFO)** and predict future noise levels based on flight operations data. We employed machine learning models to identify key factors contributing to noise exceedances and to generate accurate predictions for noise levels.

---

## Data

### Source:
- **Aircraft Noise Exceedances Dataset**: [DataSF Platform](https://data.sfgov.org/Transportation/Aircraft-Noise-Exceedances/tiju-qyvs/about_data)
- **Site ID to City Mapping**: [SFO Noise Office Reports](https://noise.flysfo.com/data-reports/published-reports/report-archive/)

### Description:
- The dataset includes information on noise levels, aircraft type, runway usage, flight operations, and spatial-temporal details.
- **Year of Analysis**: 2023
- **Cleaned Dataset**: 19,753 rows and 12 columns after processing.

---

## Methods

### Data Processing Steps:
1. **Filtering Data**:
   - Focused on records from 2023.
   - Selected only noise events caused by single SFO aircraft.
2. **Data Cleaning**:
   - Removed rows with missing values.
   - Converted timestamps to `datetime` objects.
3. **Feature Engineering**:
   - Extracted temporal features (day of the week, month).
   - Calculated the time difference between flight operations and noise events.
4. **Categorical Encoding**:
   - Applied one-hot encoding to categorical features.

### Models Used:
1. **Linear Regression**
2. **Decision Tree Regressor (CART)**
3. **Random Forest Regressor**
4. **Gradient Boosting (XGBoost)**

### Model Evaluation Metrics:
- **Mean Squared Error (MSE)**
- **R² Score**

---

## Results

- **Gradient Boosting** and **Random Forest** achieved the best performance with an **R² Score of 0.91** and low **Mean Squared Errors (3.20 and 3.31)**.
- These models outperformed Linear Regression and CART, demonstrating their effectiveness in capturing complex patterns in noise data.

---

## Impact

This project enables the prediction of future noise levels for specific neighborhoods based on flight information and runway usage. These predictions can help **airport authorities** and **urban planners** proactively manage noise pollution through optimized flight paths, scheduling adjustments, and noise abatement strategies.

---

## Future Work

- Incorporate additional data sources (weather conditions, air traffic volume).
- Explore advanced machine learning techniques (e.g., deep learning).
- Develop a user-friendly interface for real-time noise prediction.

---

## Repository Contents

- **`data/`**: Contains links to the data sources.
- **`notebooks/`**: Jupyter notebooks for data processing, EDA, and modeling.
- **`README.md`**: This file.

---
