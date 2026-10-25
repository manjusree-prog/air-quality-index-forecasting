# Air Quality Index Analysis and Prediction with Machine Learning

Analysing five years of daily air-quality data from 26 cities and building regression models that estimate the Air Quality Index (AQI) from pollutant readings and calendar features.

## Key results

| Model | R² | RMSE | MAE |
|---|---|---|---|
| Linear Regression (baseline) | 0.81 | 59.4 | 31.0 |
| **Random Forest** | **0.91** | **41.0** | **21.3** |
| Gradient Boosting | 0.90 | 43.5 | 23.7 |

Random Forest cut prediction error (RMSE) by **31%** compared with the linear baseline. **PM2.5 and CO** were by far the most important features.

## Methods

Python · pandas · NumPy · scikit-learn · Matplotlib · seaborn

- Loaded and profiled city-level and station-level datasets (daily and hourly)
- Handled missing pollutant readings with median imputation; engineered year, month, day, weekday and quarter features
- Exploratory analysis of pollution trends by city, season and AQI category
- Compared Linear Regression, Random Forest and Gradient Boosting on a held-out test set

## Notes on interpretation

AQI is calculated from pollutant concentrations, so these models estimate today's AQI from today's readings rather than forecast future values. A natural next step is true forecasting: predicting tomorrow's AQI from lagged values with time-series validation.

## Data

The notebook uses the Kaggle dataset *Air Quality Data in India (2015–2020)* (`city_day.csv` and related files). The data files are not included here; download them and place them next to the notebook.

## Author

**Teja Manjusree Koduru** · M.Sc. Big Data & Business Analytics, FOM Essen · [LinkedIn](https://www.linkedin.com/in/teja-manjusree-25856b138)
