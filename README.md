# Datasets Analysis
Analisis of Kaggle datasets with Python libraries like Scipy, Keras.

This repository is a database for most Kaggle datasets I have looked into and analysed at some point.
The results vary. Sometimes, they are satisfying, sometimes not. My main goal was not to fit the perfect
estimator, but rather look into some real-world data and display some patterns.

I have split the repository into multiple subdirectories, each for one "category" of analysis.

## 1. Regression Datasets
This folder contains some simple regression tasks as well as data preprocessing. 
The content of this folder is:
 - Car Features and MSRP - a dataset about cars, their features, and the sale price. This one contains some nice
preprocessing for comma-separated values inside columns, the estimator resulting error was around 9k, but 
a simple LinearSVR was used. When swapped to a Gaussian SVR the results would probably be way more interesting,
but my main concern on this one was data preprocessing. Dataset link - https://www.kaggle.com/CooperUnion/cardataset. 
Dataset author - CooperUnion.
