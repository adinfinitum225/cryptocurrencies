# Cryptocurrencies

## Overview

This project is an analysis of crytpocurrency data. To prepare the data for analysis categorical variables are one-hot encoded and principle component analysis is performed. The data is then classified using K-Means clustering, and is finally visualized. 

## Preprocessing

For preprocessing unnecessary columns are dropped, and categorical variables are one-hot encoded using the Pandas `get_dummies` function. The data is then scaled using the SciKit `StandardScaler`. Finally we perform principle component analysis on our data to reduce our features down to three dimensions. This reduces noise in the data and allows for later visualization using a 3D scatter plot.

## Analysis

In order to classify our data we use K-Means clustering. Plotting of an elbow curve with 1 to 11 clusters shows that 4 clusters is likely the best choice. The model is fit and the predictions are added to our dataframe. 

## Visualization

Visualization is performed using PlotlyExpress and hvPlot. To show clustering after principle component analysis a PlotlyExpress 3D scatter plot is plotted with our 3 principle components. As a final visualization hvPlot is used to plot a scatterplot of 'Total Coins Mined' vs. 'Total Coin Supply', colored by predicted class.
