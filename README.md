# Energy Consumption in Industrial Buildings: Data Analysis and Generation

## Introduction
The goal of this project was to study energy consumption data and to create data generations models from them. The data we have chosen comes from the CoSSMic project, a.k.a. Collaborating Smart Solar-powered Micro-grids.

>This data package contains measured time series data for several small businesses and residential households relevant for household- or low-voltage-level power system modeling. The data includes solar power generation as well as electricity consumption (load) in a resolution up to single device consumption. The starting point for the time series, as well as data quality, varies between households, with gaps spanning from a few minutes to entire days. All measurement devices provided cumulative energy consumption/generation over time. Hence overall energy consumption/generation is retained, in case of data gaps due to communication problems. Measurements were conducted 1-minute intervals, with all data made available in an interpolated, uniform and regular time interval. [...]
([Data description from Opne Power Source Data](https://data.open-power-system-data.org/household_data/))


The base dataset which is not included in this repository `household_data_1min_singleindex.csv`, can be found [here](https://data.open-power-system-data.org/household_data/). The documentation explaining the data is found on that same link, and additional information can be found on the [GitHub CoSSMic Project](https://github.com/isc-konstanz/household_data/tree/2020-04-15).

## The Notebooks

### data_preprocessing.ipynb
* Creation of the Daily Dataset
* Creation of the Hourly Dataset

In this Jupyter Notebook, you will find all the steps needed to generate the data subsets used in the other notebooks. Indeed, since we had at the beginning a dataset of the CO2 consumption produced per minutes in different sections of the buildings, we also wanted to have the consumption per hour and per day. The idea behind is to highlight some particular patterns within the data, for instance cycles. Cyclical phenonomena can appear on the scale of days and/or hours. This will be our focus in [SARIMA_model.ipynb](https://github.com/laurendudu/energy-consumption-data-generators#sarima_modelipynb)

### stat_descriptive.ipynb
* Visualization of Missing Values
* Study of Grid Import
* Descriptive Statistics
* Hourly Study
* Daily Study
* Weekly Study
* Monthly Study

In this notebook you will find some descriptive statistics and a first exploration of the data. 

### SARIMA_model.ipynb
* Study of the Seasonality : ACF Plots
* Rooms Consumption Prediction
* Creation of the Prediction Function

In this notebook, we will talk about the application of the SARIMA model with the data we have created previously. Based on this analyis, we will be able to study the seasonality and then predict some data.


### LSTM_lb_12.ipynb
* Data Preprocessing
* LSTM Model
* Predictions

In this notebook we fit and train an LSTM model using tensorflow. In this particular example, the lookback parameter was 12, but it can be easily changed. [Source](https://machinelearningmastery.com/time-series-prediction-lstm-recurrent-neural-networks-python-keras/)

### standard_average.ipynb
This notebook uses standard averageing for one-step ahead prediction. [Source](https://www.datacamp.com/community/tutorials/lstm-python-stock-market)






