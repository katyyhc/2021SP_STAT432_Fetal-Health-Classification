# 2021SP_STAT432_Fetal-Health-Classification

## Project Description and Summary

The goal of this project is to perform Data Analysis and Machine Learning techniques on the Cardiotocogram dataset to predict the possible classification of fetal health. Our analysis is composed of two main parts, Unsupervised Learning and Supervised Learning. Before the main analysis, we preprocess the data and transform the original dataset into two versions. In the first dataset, we perform PCA and reduce the dimensions based on PCA outcome **x_reduce**. In another dataset, we remove the categorical variable which is less informative **x_20**. 

We first perform Unsupervised Learning to understand the data and explore possible clusters without data label. The algorithms we use include K-means, Hierarchical Clustering, and Self-Organizing Map. Among these three methods, Self-Organizing Map outperforms the other two methods. We also perform these clustering methods on both two preprocessed datasets, and the outcome shows that **x_20** can better identify the clusters than **x_reduce**. With this initial outcome, we use **x_20** for Supervised Learning. We apply SVM, Random Forests, and Boosting to predict the fetal health classification, and find that the tree based XGBoost model reaches the best outcome. In addition, for all the three models, classification accuracy of Class 2 is the lowest, which might because the true fetal health status of observations in “suspect” category are relatively difficult to recognize.

## Methods

Unsupervised Learning:
* K-means
* Hierarchical Clustering
* Self-Organizing Map

Supervised Learning:
* SVM
* Random Forest
* XGBoost
