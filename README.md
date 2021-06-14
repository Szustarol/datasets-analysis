# Datasets Analysis
Analysis of Kaggle datasets with Python libraries like Scipy, Keras.

This repository is a database for most Kaggle datasets I have looked into and analysed at some point.
The results vary. Sometimes, they are satisfying, sometimes not. My main goal was not to fit the perfect
estimator, but rather look into some real-world data and display some patterns.

I have split the repository into multiple subdirectories, each for one "category" of analysis.

## 1. Regression Datasets
This folder contains some simple regression tasks as well as data preprocessing. 
The content of this folder is:
 - [Car Features and MSRP](https://github.com/Szustarol/datasets-analysis/tree/master/Regression%20Datasets/Car%20Features%20and%20MSRP) - a dataset about cars, their features, and the sale price. This one contains some nice
preprocessing for comma-separated values inside columns, the estimator resulting error was around 9k, but 
a simple LinearSVR was used. When swapped to a Gaussian SVR the results would probably be way more interesting,
but my main concern on this one was data preprocessing.
Dataset link - https://www.kaggle.com/CooperUnion/cardataset. 
Dataset author - CooperUnion.
 - [Diamonds](https://github.com/Szustarol/datasets-analysis/tree/master/Regression%20Datasets/Diamonds) - a dataset containing information about diamonds, and their price as the target. For this one,
preprocessing isn't problematic, I just wanted to measure how good of a fit I can get with this dataset.
The relative error achieved was around 4.5%, which is quite a good estimation.
Dataset link - https://www.kaggle.com/shivam2503/diamonds
Dataset author - Shivam Agraval.

## 2. Classification Datasets
This folder contains datasets for which the task I have estabilished was to predict a class.
The content of this folder is:
 - [Titanic](https://github.com/Szustarol/datasets-analysis/tree/master/Classification%20Datasets/Titanic) - classic ML dataset. The goal is to predict if a passenger of Titanic survived the sinking ship. This dataset is interesting because it is relatively small, so prediction is not easy. Using RandomForestClassifier and some non-basic preprocessing, I was able to achieve almost 80% accuracy, which is the top 7% on Kaggle.
Dataset link - https://www.kaggle.com/c/titanic/overview
Dataset author - Kaggle
 - [Mail spam detection](https://github.com/Szustarol/datasets-analysis/tree/master/Classification%20Datasets/Spam) - classification of emails - spam or ham. This dataset was provided by Apache SpamAssassin. I have been able to achieve accuracy of 96%, with almost equal number of ham and spam examples in the dataset. The training and testing data contains both easy and hard examples from the Apache website.
Dataset link - https://spamassassin.apache.org/old/publiccorpus/
 - [Mushrooms](https://github.com/Szustarol/datasets-analysis/tree/master/Classification%20Datasets/Mushrooms) - a very simple, nice to work with mushroom dataset, the target is to predict if a mushroom is edible. This dataset is really easy to fit with 100% accuracy, but what is nice about it is not a high score, but that this high score can be achieved by using a Random Forest Classifier, giving the user an insight about how different features affect edibility.
Dataset link - https://www.kaggle.com/uciml/mushroom-classification
Dataset author - UCI Machine Learning
