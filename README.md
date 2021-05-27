# 2021SP_STAT432_Fetal-Health-Classification

## Project Description and Summary

The goal of this project is to perform Data Analysis and Machine Learning techniques on the Cardiotocogram dataset to predict the possible classification of fetal health. Our analysis is composed of two main parts, Unsupervised Learning and Supervised Learning. Before the main analysis, we preprocess the data and transform the original dataset into two versions. In the first dataset, we perform PCA and reduce the dimensions based on PCA outcome **x_reduce**. In another dataset, we remove the categorical variable which is less informative **x_20**. 

We first perform Unsupervised Learning to understand the data and explore possible clusters without data label. The algorithms we use include K-means, Hierarchical Clustering, and Self-Organizing Map. Among these three methods, Self-Organizing Map outperforms the other two methods. We also perform these clustering methods on both two preprocessed datasets, and the outcome shows that **x_20** can better identify the clusters than **x_reduce**. With this initial outcome, we use **x_20** for Supervised Learning. We apply SVM, Random Forests, and Boosting to predict the fetal health classification, and find that the tree based XGBoost model reaches the best outcome. In addition, for all the three models, classification accuracy of Class 2 is the lowest, which might because the true fetal health status of observations in “suspect” category are relatively difficult to recognize.

## Methods

### Unsupervised Learning:
* K-means
* Hierarchical Clustering
* Self-Organizing Map

### Supervised Learning:
* SVM
* Random Forest
* XGBoost

## Evaluation

### Unsupervised Learning:

<p align="center"><img src="https://user-images.githubusercontent.com/59358509/119888906-8c9b7880-befb-11eb-914e-906fdda76530.png" width="400" height="120">

* The highest and the lowest accuracy are both obtained using the SOM algorithm with the **x_20** and **x_reduce** dataset, respectively. 
* Among the three algorithms, K-Means appears to have a worse performance. 
* The clustering accuracy of the three algorithms are all higher when using **x_20** compared to using **x_reduce**.

### Supervised Learning:

<p align="center"><img src="https://user-images.githubusercontent.com/59358509/119897798-94ace580-bf06-11eb-9fd9-e4dfa85c990b.png">

* Among all of the models, the tree based XGBoost model reaches the best outcome— 93.05% accuracy and 97.74% AUC.
* Among SVM models, the one with rbf kernel outperforms the other two and reaches 91.92% accuracy and 97.37% AUC.  
* Random Forest also achieves a satisfying performance with 90.6% accuracy and 97.28% AUC. 
* Almost all of the models tend to perform worse in classifying observations from fetal_health status 2 correctly, indicated by a much lower sensitivity of class 2 compared to the other two classes.
