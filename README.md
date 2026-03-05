# Cinnamon Export Forecasting

**Project:** Comparative analysis of forecasting models for monthly Ceylon cinnamon exports in Sri Lanka.  
**Goal:** Determine the most accurate short-term forecasting method for the Sri Lanka monthly Ceylon cinnamon export dataset (2004–2025) to support strategic planning.

**Technologies & Methods:** Python, R, EViews, SARIMA, Artificial Neural Networks (ANN), Fuzzy Time Series, Time Series Analysis, Pandas, NumPy, TensorFlow, Statsmodels, Data Visualization (Matplotlib)

---

## Project Overview

Sri Lanka is the world’s largest producer of pure cinnamon. Accurate forecasting of export quantities helps exporters and policymakers make informed decisions. This project compares **SARIMA**, **ANN**, and **Fuzzy Time Series** models to determine the best short-term forecasting approach.

---

## Dataset

- **Source:** Sri Lanka Export Development Board (SLEDB)  
- **Period:** Jan 2004 – Jun 2025  
- **Granularity:** Monthly exports (tonnes)  

<img width="687" height="380" alt="image" src="https://github.com/user-attachments/assets/63307a3b-c77a-4637-b027-daec40bcb861" />

---

## Methodology

1. **Data Preprocessing:** Handled missing values, aggregated monthly export quantities across product categories, standardized data for ANN  

2. **Exploratory Data Analysis (EDA):** Identified trends and seasonality using visual analysis and statistical tests (ADF). Differencing was applied to achieve stationarity.  

3. **Forecasting Models**

   - **SARIMA:** Model parameters selected using Auto ARIMA and diagnostic tests to capture seasonal patterns and trends in the data.
   
   - **Artificial Neural Network (ANN):** Feed-forward neural network using lagged inputs. Hyperparameters such as input lags, number of neurons, hidden layers, batch size, and learning rate were tuned using trial and error, based on training and validation loss curves.
   
   - **Fuzzy Time Series (Singh, 2008):** Multiple interval partitions were tested, and the optimal model was selected based on **RMSE, MAE, and MAPE** performance.

4. **Evaluation:** Model performance compared using **RMSE, MAE, and MAPE**.

---

### SARIMA Forecast vs Actual (Test Set)

<img width="708" height="437" alt="image" src="https://github.com/user-attachments/assets/838acbd2-a64f-4497-be6b-8d28fc4d8ed6" />

### ANN Forecast vs Actual (Test Set)

<img width="730" height="353" alt="image" src="https://github.com/user-attachments/assets/feff0075-8840-46f7-a41a-9911e7e4bb2a" />

### Fuzzy Time Series Forecast vs Actual (Test Set)

<img width="726" height="322" alt="image" src="https://github.com/user-attachments/assets/684052fd-a36f-4ac5-93e1-32058f40dbb2" />

---

## Results Highlights

| Model | RMSE   | MAE    | MAPE    |
|-------|--------|--------|---------|
| SARIMA | 299.75 | 256.03 | 16.95% |
| ANN    | 318.55 | 249.02 | 28.21% |
| Fuzzy  | 354.60 | 296.61 | 19.80% |

**Key Insight:** SARIMA performed best due to clear linear trend and seasonality present in the ceylon cinnamon export data.

---

### SARIMA Forecast for the Next 3 Months

<img width="657" height="400" alt="image" src="https://github.com/user-attachments/assets/013899c5-0f2e-447d-999c-646e02591446" />

---

## Folder Structure

cinnamonExport-sarima-ann-fuzzyTimeSeries/

│

├── data/

│   ├── raw/

│   └── processed/

├── notebooks/

│   ├── modeling.ipynb

│   └── sarima_analysis.Rmd

├── figures/

├── results/

├── .gitignore

└── README.md





