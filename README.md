# MLLB Project (Machine and Deep Learning)

This repository will present the experiments I made using classical machine learning techniques and deep learning techniques to predict the air quality in areas of the city of Barcelona given the past and present road traffic and weather. Once this is achieved, it can be easily used to predict the air quality in the upcoming hours (even days), because road traffic can be easily predicted and weather forecast can be fetched from weather services.


## Files in this repository

| File | Use |
| --- | --- |
| `dataset_creation.ipynb` | Creates the dataset files (regression and classification) used by `exploratory_data_analysis.ipynb`. |
| `exploratory_data_analysis.ipynb `| Performs the EDA, and cleans the datasets accordingly, creating the final datasets, used by all next notebooks.|
| `regression_main.ipynb` | Train and test a regression model to predict traffic, and another to predict PM10 concentration in the air, with 12 hours overhead |
| `classification_main.ipynb` | Similar to the previous one, the traffic predictor is unchanged, the air quality model is now using labels |
| `deep_learning_naive.ipynb` | Train and test a deep learning model to predict traffic, and another to predict PM10 concentration in the air, with 12 hours overhead, using a feed-forward NN with lags and rolls in the dataset (my first, naive experiment)|
| `deep_learning_improved.ipynb` | Train and test a deep learning model to predict traffic, and another to predict PM10 concentration in the air, with 12 hours overhead, this time using a version of the dataset whithout lags and rolls, and a model adapted to time series (1D-CNN, GRU, LSTM) |


I also include directly in the repository the `.pkl` file, so it is not mandatory to run the first two notebooks.

## Future work
I plan on trying many more methods for machine learning (optimization of parameters through grid search, comparizon of models...) and deep learning (effects of the parameters, shape/type of the network...)

This repository is basically a functional template for future work, as I spent most of my time working on the creation of the dataset.
