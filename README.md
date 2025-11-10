# Predicting Air Quality in Barcelona (MLLB Report)

This repository contains the code, data processing codes, and experimental results for the Predicting Air Quality in Barcelona project, conducted as a report for the MLLB (Machine Learning Laboratory) course.

The goal of this project is to develop and evaluate deep learning models (and compare them with classical machine learning approaches) to predict hourly air quality (specifically PM10 concentrations) hours in the future across Barcelona.

This project includes:
- A dataset creation notebook : Code for gathering, cleaning, and merging large datasets from the Barcelona OpenData portal and the Open-Meteo API, including:

  - Hourly Air Quality measurements from 8 stations.

  - Hourly Road Traffic Density from hundreds of sections, aggregated into a configurable city grid.

  - Hourly Weather Data (temperature, wind, precipitation, etc.).

- Exploratory Data Analysis (EDA): Detailed analysis confirming data health, identifying sensor anomalies, and establishing correlations between traffic, weather, and air pollution.

- Model Implementation:

  - Classical Machine Learning: Gradint Boosting for initial traffic prediction.

  - Deep Learning (DL) Models: Sequential Dense Neural Networks for predicting air quality régression and classification targets.

## Files in this repository

| File | Use |
| --- | --- |
| `dataset_creation.ipynb` | Creates the dataset files (regression and classification) used by `exploratory_data_analysis.ipynb`. |
| `exploratory_data_analysis.ipynb `| Performs the EDA, and cleans the datasets accordingly, creating the final datasets, used by all next notebooks.|
| `regression_main.ipynb` | Train and test a regression model to predict traffic, and another to predict PM10 concentration in the air, with 12 hours overhead |
| `classification_main.ipynb` | Similar to the previous one, the traffic predictor is unchanged, the air quality model is now using labels |
| `deep_learning_main.ipynb` | Train and test a deep learning model to predict traffic, and another to predict PM10 concentration in the air, with 12 hours overhead |


I also include directly in the repository the `.pkl` file, so it is not mandatory to run the first two notebooks.

## Future work
I plan on trying many more methods for machine learning (optimization of parameters through grid search, comparizon of models...) and deep learning (effects of the parameters, shape/type of the network...)

This repository is basically a functional template for future work, as I spent most of my time working on the creation of the dataset.
