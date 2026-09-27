# sky-predict
"A Python-based machine learning pipeline to forecast weather conditions and predict daily temperatures using historical climate data."
# Weather Forecasting Using Machine Learning

A beginner-friendly Python project that uses historical weather observations and Linear Regression to estimate temperature from humidity, pressure, wind speed, and rainfall.

## Important dataset note
The included `data/weather.csv` is a **synthetically generated educational dataset** with 1,826 daily observations from 2021-01-01 through 2025-12-31. It is included so the repository runs immediately and does not falsely present fabricated observations as real-world measurements. For an academic submission requiring a real public dataset, replace it with a documented historical dataset and update the report references/results.

## Features
- CSV loading and validation
- Data cleaning
- Exploratory visualizations
- Linear Regression
- 80/20 train-test split
- MAE, MSE, RMSE and R² evaluation
- New-input temperature prediction
- Automated output CSV files
- Unit test

## Run
```bash
pip install -r requirements.txt
python src/main.py
```

## Test
```bash
pytest
```

## Project structure
- `data/` dataset
- `src/` application modules
- `tests/` automated test
- `outputs/` generated metrics, plots and prediction results
- `diagrams/` project diagrams
- `report/` report document
- `presentation/` presentation
- `viva/` viva questions and answers

## Model
Input features: Humidity, Pressure, WindSpeed, Rainfall  
Target: Temperature  
Algorithm: Linear Regression

## Academic disclaimer
This is an educational machine-learning project and is not a professional weather forecasting system.
