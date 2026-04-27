# Air-Quality-Index-Prediction-Using-Random-Forest-and-Decision-Tree-
Created an Interface for User to check the Air Quality.
A machine learning project that predicts Air Quality Index (AQI) category based on pollutant input values.

## About the Project

This project takes pollutant values as user input, predicts the AQI category using trained ML models, and displays confidence scores and pollutant status against safe limits.


## Dataset

- File: `cleaned_project_dataset.csv`
- Target: `AQI_Bucket`
- Features: PM2.5, PM10, NO, NO2, NOx, NH3, CO, SO2, O3, Benzene, Toluene, Xylene


## AQI Categories

| Category    | Color  |
|-------------|--------|
| Good        | Green  |
| Satisfactory| Blue   |
| Moderate    | Orange |
| Poor        | Red    |
| Very Poor   | Purple |
| Severe      | Navy   |


## Safe Limits

| Pollutant | Safe Limit |
|-----------|-----------|
| PM2.5     | 75        |
| PM10      | 100       |
| NO        | 40        |
| NO2       | 40        |
| NOx       | 80        |
| NH3       | 30        |
| CO        | 2         |
| SO2       | 20        |
| O3        | 100       |
| Benzene   | 5         |
| Toluene   | 10        |
| Xylene    | 10        |


## Libraries Used

| Library              | Purpose                  |
|----------------------|--------------------------|
| pandas               | Data handling            |
| matplotlib           | Plotting charts          |
| sklearn.model_selection | Train/test split      |
| sklearn.preprocessing   | StandardScaler        |
| sklearn.ensemble        | RandomForestClassifier|
| sklearn.tree            | DecisionTreeClassifier|
| sklearn.metrics         | accuracy_score        |

## Models

| Model                        | Accuracy |
|------------------------------|----------|
| Decision Tree (max_depth=4)  | 73.35%   |
| Random Forest (n_estimators=100) | 81.25% |

- Train/Test Split: 80% / 20%
- Best Model: **Random Forest**


## Sample Output

| Pollutant | Your Value | Safe Limit | Status |
|-----------|-----------|------------|--------|
| PM2.5     | 28.00     | 75.0       | OK     |
| PM10      | 52.00     | 100.0      | OK     |
| NO        | 10.00     | 40.0       | OK     |
| NO2       | 18.00     | 40.0       | OK     |
| NOx       | 0.80      | 80.0       | OK     |
| NH3       | 25.00     | 30.0       | OK     |
| CO        | 0.80      | 2.0        | OK     |
| SO2       | 10.00     | 20.0       | OK     |
| O3        | 55.00     | 100.0      | OK     |
| Benzene   | 1.20      | 5.0        | OK     |
| Toluene   | 4.00      | 10.0       | OK     |
| Xylene    | 3.00      | 10.0       | OK     |

Prediction: **Satisfactory** (56% confidence)

## CONCLUSION
The AQI Predictor uses 12 pollutant features to classify air quality into six categories, with Random Forest achieving 81.25% accuracy compared to Decision Tree's 73.35%, making it the better model. The project takes real pollutant values as user input, checks each against safe limits, and predicts the AQI category along with confidence scores for every possible outcome. Overall, this project demonstrates how machine learning can effectively analyze environmental pollutant data to deliver fast, reliable, and interpretable air quality predictions.
