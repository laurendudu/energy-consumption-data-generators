# Energy Consumption in Industrial Buildings : Data Analysis and Generation

## Introduction

## The Notebooks

### Data Preprocessing : Creation of the Daily and the Hourly Datasets : 

### data_preprocessing.ipynb
* Creation of the Daily Dataset
* Creation of the Hourly Dataset

In this Jupyter Notebook, you will find all the steps we did to obtain the two datasets. Indeed, since we had at the beginning a dataset of the CO2 consumption produced per minutes in different sections of the buildings, we also wanted to have the consumption per hour and per day. The idea behind is to highlight some particluar patterns within the data, for instance cycles. Cyclical phenonomena can appear on the scale of days and/or hours. This will be our focus in the next Jupyter Notebook. 

### SARIMA Model : Data Analysis and Prediction

### SARIMA_model.ipynb
* Study of the Seasonality : ACF Plots
* Rooms Consumption Prediction
* Creation of the Prediction Function

In this section, we will talk about the application of the SARIMA model with the data we have created previously. Based on this analyis, we will be able to study the seasonality and then predict some data based on it.  
