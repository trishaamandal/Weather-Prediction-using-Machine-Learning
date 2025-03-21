# Weather-Prediction-using-Machine-Learning-Python-
This repository contains a Python project that performs weather prediction using machine learning techniques. The project utilizes the pandas library to read and manipulate weather data from a CSV file and implements a Ridge regression model for making predictions. The goal of this project is to forecast the maximum temperature (temp_max) for future dates based on historical weather data.

Dataset:
The weather data is loaded from a CSV file named "local_weather.csv" using pandas. The data contains various weather-related attributes such as precipitation, snowfall, snow depth, maximum temperature (temp_max), and minimum temperature (temp_min).

Data Preprocessing:
The data is preprocessed to handle missing values. The percentage of missing values in each column is calculated and displayed. The columns "snow" and "snow_depth" are mostly empty and are thus removed from the dataset. The missing values in the "precipitation," "temp_max," and "temp_min" columns are filled with their respective average values.

Exploratory Data Analysis (EDA):
EDA is performed on the dataset, and plots are generated to visualize the trends in minimum and maximum temperatures over time.

Machine Learning Model:
A Ridge regression model is chosen for the weather prediction task. The predictors used for the model are "temp_max," "temp_min," and "precipitation," while the target variable is the shifted "temp_max" column, which represents the maximum temperature for the next day. The dataset is split into a training set (historical data up to 2020-12-31) and a test set (data from 2021-01-01 onwards).

Model Training and Prediction:
The Ridge regression model is trained on the training set using the selected predictors to predict the target variable. The trained model is then used to make predictions on the test set. The mean absolute error (MAE) is calculated to evaluate the performance of the model on the test set.

Analysis Table:
An analysis table is created to compare the actual maximum temperatures (target) in the test set with the predicted values from the model. The table provides insights into the accuracy of the predictions.

Predictions Generator Function:
The project also includes a function named "predictions_generator" that encapsulates the model training and prediction process. This function takes the predictors, dataset, and Ridge regression model as inputs and returns the mean absolute error and the analysis table for the predictions.

This project serves as a practical example of weather prediction using machine learning techniques and can be extended to explore other models or additional features for more accurate forecasting.
