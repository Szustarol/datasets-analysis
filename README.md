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
 - [CIFAR10](https://github.com/Szustarol/datasets-analysis/tree/master/Classification%20Datasets/CIFAR10) - another very simple testing on the CIFAR10 dataset - trying to determine how well can a non-recursive, non-convolutional network fit it. The score was around 52%, which is of course not good, but in pair with other tests on this dataset, performed by other people. This demonstrates the lack of variance in the standard dense neural networks when it comes to this kind of task.

## 3. Implementation
This folder contains my implementation of various machine learning algorithms, and a comparison of their results on classic ML datasets.
The content of this folder is:
 - [Softmax for MNIST](https://github.com/Szustarol/datasets-analysis/master/Implementation/Softmax) - implementation of the Softmax Logistic Regression and a test on the MNIST
 dataset, compared to the Sklearn version. Whith the regularized (l1/l2) implementation I was able to achieve around 90.94% accuracy, Sklearn reached 91.15% (but with a long training time), and mini-batch early-stopping implementation with learning schedule was able to achieve 91.78% accuracy.
 - [SVM for Iris](https://github.com/Szustarol/datasets-analysis/master/Implementation/SVM) - implementation of SVM classification with a RBF kernel. The quadratic problem solver I have used was supplied by the CVXOPT Python library. On the Iris dataset, as expected, I was able to achieve high prediction scores, although they were strongly dependant on the train/test split. Overall, It is possible to achieve >95% accuracy, with 100% accuracy achieved as an example (though probably not a well-scaling one).
 - [CART (Decision Tree) on the wine dataset](https://github.com/Szustarol/datasets-analysis/master/Implementation/CART) - Even though this dataset is relatively small, my implementation of a single decision tree was able to reach around 83.8% accuracy score, as a mean of 10 cross-validations, which is not bad at all for a single tree. In comparison, the scikit-learn implementation achieved a mean score of 87% - i don't consider this score to be poor, since my implementation is very basic without any advanced criteria. What was interesting though, is that PCA didn't seem to improve the results. Also, for some reason, my tree seems to be more less stable than the scikit-learn one, but when number of cross validation was greater than 20, both implementations reached a score of 89%.
 - [AdaBoost and Gradient Boosting](https://github.com/Szustarol/datasets-analysis/master/Implementation/Boosting) - Implementation of AdaBoost and GradientBoosting algorithms, as simple as the implementations are, they both achieve exactly the same cross-val score as scikit-learn.
 - [Multilayer Perceptron](https://github.com/Szustarol/datasets-analysis/master/Implementation/MLP) - A very basic implementation of multilayer perceptron neural network, tested on the breast cancer dataset. The achieved accuracy after 100 epochs was ~96% - for comparison, the same network structure with Keras achieved 92%, but this is possibly due to regularization.
