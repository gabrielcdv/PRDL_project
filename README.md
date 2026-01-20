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
| `deep_learning_naive.ipynb` | Train and test a deep learning model to predict traffic, and another to predict PM10 concentration in the air, with 12 hours overhead, using a feed-forward NN with lags and rolls in the dataset (my first, naive experiment)|
| `deep_learning_improved.ipynb` | Train and test a deep learning model to predict traffic, and another to predict PM10 concentration in the air, with 12 hours overhead, this time using a version of the dataset whithout lags and rolls, and a model adapted to time series (1D-CNN, GRU, LSTM) |


I also included directly in the repository the `.pkl` files, so it is not mandatory to run the first two notebooks.

## Technical details
This project was written on my personal computer using Python 3.13.7.
The first notebook **cannot** be executed on Google Colab because it downloads data from Barcelona's OpenData server, which blocks requests from Colab machines. The other notebooks should run fine as the datasets files are included in the repository.
## Future work
I plan on trying many more methods for machine learning (optimization of parameters through grid search, comparizon of models...) and deep learning (effects of the parameters, shape/type of the network...)

This repository is basically a functional template for future work, as I spent most of my time working on the creation of the dataset.
