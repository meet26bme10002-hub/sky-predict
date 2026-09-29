# WEATHER FORECASTING USING MACHINE LEARNING

## A Project Report

**Submitted by:** Your Name  
**Roll Number:** Your Roll Number  
**Course:** Your Course Name  
**Semester:** 1st Semester  
**College:** Your College Name  
**Academic Year:** 2026–27

> Replace the four personal placeholders above before submission.

## 1. Abstract
This project presents a beginner-friendly weather forecasting application developed in Python. Historical daily weather observations are processed using Pandas, visualized using Matplotlib, and used to train a Linear Regression model with Scikit-learn. The model uses humidity, pressure, wind speed, and rainfall as input features and temperature as the target variable. The application evaluates the model using Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and R². It also accepts new weather values from the user and produces a temperature estimate.

## 2. Introduction
Weather conditions change continuously and are influenced by several measurable environmental factors. Machine learning provides a simple way to learn relationships from historical observations. This project demonstrates the complete basic workflow: data collection/storage, cleaning, analysis, visualization, model training, evaluation, and prediction.

## 3. Problem Statement
Traditional meteorological forecasting can involve complex scientific models and large datasets. The objective here is not to replace professional systems, but to demonstrate how a simple supervised regression model can learn relationships among weather variables and estimate temperature.

## 4. Objectives
- Read historical weather data from CSV.
- Validate required columns and clean missing/invalid values.
- Visualize temperature and humidity.
- Train a Linear Regression model.
- Evaluate model performance.
- Predict temperature for user-provided weather conditions.
- Demonstrate modular programming, testing, documentation, and version control.

## 5. Scope
The application covers CSV input, preprocessing, visualization, regression, evaluation, and prediction. It does not attempt severe-weather prediction, professional real-time forecasting, simultaneous prediction of every weather variable, or deep learning.

## 6. Functional Requirements
1. **Data Input:** Load and validate a CSV dataset.
2. **Data Processing:** Convert data types and remove unusable rows.
3. **Visualization:** Generate temperature and humidity plots.
4. **ML Prediction:** Train Linear Regression and estimate temperature.
5. **Evaluation:** Calculate MAE, MSE, RMSE and R².

## 7. Non-Functional Requirements
- **Performance:** Process a student-sized dataset within seconds.
- **Usability:** Provide clear command-line prompts.
- **Reliability:** Handle missing files, columns, and invalid numeric input.
- **Maintainability:** Separate functionality into modules.
- **Resource Efficiency:** Run on a normal laptop without a GPU.
- **Error Handling:** Display understandable error messages.

## 8. Technology Stack
| Technology | Purpose |
|---|---|
| Python | Main language |
| Pandas | Data processing |
| NumPy | Numerical operations |
| Matplotlib | Visualization |
| Scikit-learn | Machine learning |
| CSV | Lightweight data storage |
| Git/GitHub | Version control/repository hosting |

## 9. Dataset
The included dataset contains **1,826 daily observations** from **2021-01-01 to 2025-12-31**. The repository identifies it as a **synthetic educational dataset**, generated solely so the project can run reproducibly without misrepresenting fabricated values as real observations.

Columns:
- Date
- Temperature
- Humidity
- Pressure
- WindSpeed
- Rainfall

Features: Humidity, Pressure, WindSpeed, Rainfall  
Target: Temperature

## 10. Machine Learning Method
The project uses supervised learning because each training row contains input features and a known target temperature. The task is regression because temperature is a continuous numerical output.

Linear Regression models the target approximately as:

`Temperature = b0 + b1(Humidity) + b2(Pressure) + b3(WindSpeed) + b4(Rainfall)`

An 80/20 train-test split is used with `random_state=42`.

## 11. System Architecture
See `diagrams/system_architecture.txt`.

User → Interface → Dataset → Preprocessing → Visualization/Model Training → Evaluation → Prediction.

## 12. Workflow
See `diagrams/workflow.txt`.

The workflow loads data, validates it, cleans it, selects features, splits training/testing data, trains the model, predicts test values, evaluates performance, accepts new inputs, and produces a prediction.

## 13. Design Diagrams
The repository contains:
- Use Case Diagram
- Workflow Diagram
- Sequence Diagram
- Class/Component Diagram
- System Architecture Diagram

## 14. Implementation Details
The code is divided into:
- `data_processor.py`: loading, validation, cleaning and feature preparation.
- `model.py`: splitting, training, prediction and evaluation.
- `visualizer.py`: graph generation.
- `predictor.py`: new-input prediction.
- `main.py`: application orchestration.

## 15. Model Results
The results below were generated from the included dataset and the actual implementation.

| Metric | Value |
|---|---:|
| MAE | 0.7012
| MSE | 0.7684
| RMSE | 0.8766
| R² | 0.7390

The values are dataset-specific and should be recalculated if the dataset is replaced.

## 16. Output Files
- `outputs/temperature_plot.png`
- `outputs/humidity_plot.png`
- `outputs/actual_vs_predicted.png`
- `outputs/prediction_results.csv`
- `outputs/metrics.csv`

## 17. Testing
| Test Case | Input | Expected Result |
|---|---|---|
| TC01 | Valid CSV | Dataset loads |
| TC02 | Missing CSV | Error message |
| TC03 | Valid weather values | Temperature prediction |
| TC04 | Text instead of number | Input validation error |
| TC05 | Missing required column | Validation error |
| TC06 | Model training | Model trains and predicts |

Automated test:
`pytest`

## 18. Challenges Faced
- Cleaning and validating tabular data.
- Understanding training versus testing data.
- Selecting relevant features.
- Understanding regression evaluation metrics.
- Learning APIs from Pandas and Scikit-learn.
- Organizing the application into multiple modules.

## 19. Learnings
The project demonstrates data handling with Pandas, visualization, supervised regression, train/test evaluation, modular programming, testing, documentation, and Git/GitHub workflow.

## 20. Future Enhancements
- Use a documented real-world weather dataset.
- Add real-time weather APIs.
- Compare multiple ML algorithms.
- Add rainfall/humidity prediction.
- Add a graphical interface.
- Develop a web application.
- Add database support.
- Add automatic daily forecasting.
- Experiment with advanced time-series models.
- Deploy online.

## 21. Limitations
This is an educational demonstration, not a professional forecasting system. The included dataset is synthetic and should not be interpreted as measured weather history. Linear Regression also simplifies potentially nonlinear relationships.

## 22. Conclusion
The project demonstrates a complete beginner-level machine-learning workflow for temperature estimation. It combines data preprocessing, visualization, regression, evaluation, prediction, testing, and documentation in a modular Python application.

## 23. References
- Python Documentation — https://docs.python.org/
- Pandas Documentation — https://pandas.pydata.org/docs/
- NumPy Documentation — https://numpy.org/doc/
- Matplotlib Documentation — https://matplotlib.org/stable/
- Scikit-learn Documentation — https://scikit-learn.org/stable/
- Dataset documentation: included dataset generation note in this repository.

## 24. Submission Checklist
- [ ] Replace personal placeholders.
- [ ] Review dataset choice against college requirements.
- [ ] Run `pip install -r requirements.txt`.
- [ ] Run `pytest`.
- [ ] Run `python src/main.py`.
- [ ] Review generated outputs.
- [ ] Add screenshots if your college requires them.
- [ ] Initialize Git and push the repository.
