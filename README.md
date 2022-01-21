# Energy Consumption in Industrial Buildings : Data Analysis and Generation

## Introduction
This project studies 

The base dataset which is not included in this repository `household_data_1min_singleindex.csv`, can be found [here](https://data.open-power-system-data.org/household_data/). The documentation explaining the data is found on that same link, and additional information can be found on the [GitHub CossMic Project](https://github.com/isc-konstanz/household_data/tree/2020-04-15).

## The Notebooks

### data_preprocessing.ipynb
* Creation of the Daily Dataset
* Creation of the Hourly Dataset

In this Jupyter Notebook, you will find all the steps we did to obtain the two datasets. Indeed, since we had at the beginning a dataset of the CO2 consumption produced per minutes in different sections of the buildings, we also wanted to have the consumption per hour and per day. The idea behind is to highlight some particluar patterns within the data, for instance cycles. Cyclical phenonomena can appear on the scale of days and/or hours. This will be our focus in the next Jupyter Notebook. 

### stat_descriptive.ipynb
* Visualization of Missing Values
* Study of Grid Import
* Descriptive Statistics
* Hourly Study
* Daily Study
* Weekly Study
* Monthly Study

### SARIMA_model.ipynb
* Study of the Seasonality : ACF Plots
* Rooms Consumption Prediction
* Creation of the Prediction Function

In this notebook, we will talk about the application of the SARIMA model with the data we have created previously. Based on this analyis, we will be able to study the seasonality and then predict some data based on it.  


### LSTM_lb_12.ipynb
* Data Preprocessing
* LSTM Model
* Predictions

### standard_average.ipynb






