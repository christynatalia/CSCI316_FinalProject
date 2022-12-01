# CSCI316_FinalProject - Credit Risk Analysis

## Table of Contents
1. [ About the Project ](#about)
2. [ Problem Description ](#desc)
3. [ Methods ](#methods)
4. [ Conclusion ](#conclusion)


<a name="about"></a>
### 1. About the Project
This is a group project by Christy, Clarissa, Eva, Raveena, and Yuin for CSCI316 Big Data Mining and Implementation course. 

<a name="desc"></a>
### 2. Problem Description
We are given a dataset called credit risk analysis. This dataset consists of 73 columns and more than 8 million rows. However, it has many missing values and some outliers. The purpose of this project is to predict whether credit needs to be given or not based on several features. 

<a name="methods"></a>
### 3. Methods
We use Python as the language for making this project and implements pyspark which is the big data processing framework. Since this is a regression problem, there are several algorithms used by implementing the libraries from tensorflow and pyspark. Here are the list:

* ## TensorFlow

  * Feedforward Neural Network
  * Support Vector Machine
  * Random Forest
  * Decision Tree
  * Gradient Boosted Trees
  

* ## PySpark

  * Naive Bayes
  * Random Forest
  * Decision Tree
  
<a name="conclusion"></a>
### 4. Conclusion
 
 * ## Tensorflow
<img width="596" alt="Screen Shot 2022-12-01 at 11 51 00" src="https://user-images.githubusercontent.com/57931555/204939358-86fc45bf-95cb-453f-a286-e55729411261.png">
SVM is the least optimal model for this dataset. All four models except SVM comparatively do not have a high number of false positives as well here.

However, there is some abnormalities here. In theory, it says that the random forest accuracy must be higher than decision tree whereas it is not here. The reason as to why is because of overfitting and the model that we built is too complex. To overcome this problem, we have to implement grid search to test out the suitable parameters but we don’t have sufficient computational power and time. Then if we look at the metrics for feedword neural network and gradient boosted trees, both of them have performed really well. FNN is a has an advantage of having the ability to represent more complex functions very easily. However, it is more prone to overfitting due to weight-sharing between nodes of the network. FNN has more number of false positives compared to GBT. So we would like to identify GBT as our best performing tensorflow model.

 * ## PySpark
 
<img width="305" alt="Screen Shot 2022-12-01 at 12 58 43" src="https://user-images.githubusercontent.com/57931555/204947718-97a60c3e-95f4-4202-8e5d-47a4951de970.png">
All three models comparatively do not have a high number of false positives which is very vital to us. Naive Bayes is the worst because it has the lowest accuracy, recall and f1 score. A reason as to why is because it does not take into account the possible correlation between other features. There were higher false negatives which explains why its precision is lower than the other models as well. From all aspects, both Decision tree and Random Forest performed pretty well but random forest has yielded the best results.This is because it is less prone to overfitting than Decision Tree. Both models have predicted all the positive samples correctly. Therefore, the f1 score is higher which is pretty important to us to minimize credit risk.


