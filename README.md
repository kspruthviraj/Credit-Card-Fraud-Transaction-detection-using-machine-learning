# Credit-Card-Fraud-Transaction-detection-using-machine-learning


##Introduction
To build machine learning models to detect fraudulent card transactions


#Data Description
We make use of the credit card data(https://www.kaggle.com/mlg-ulb/creditcardfraud/data) that consists of two-days credit card transactions made in September 2013 by European cardholders. The dataset is highly unbalanced with a low percentage of fraudulent transactions within several records of normal transactions. The positive class (frauds) account for 0.172% (492 frauds out of 284,807 transactions) of all transactions.

Features V1, V2, V3..., V28 are the principal components that have been extracted using Principal component analysis, whereas the features 'Time' and 'Amount' are in its original form. Feature 'Time' contains the seconds elapsed between each transaction and the first transaction in the dataset. Feature 'Class' is the target variable with value 1 in case of fraud and 0 otherwise.


To compensate for the imbalance in dataset, we will use ADASYN oversampling method by importing imbalanced-learn package to resample the dataset.  
ADASYN (ADAptive SYNthetic) is an [oversampling technique](https://www.datasciencecentral.com/profiles/blogs/handling-imbalanced-data-sets-in-supervised-learning-using-family) that adaptively generates minority data samples according to their distributions using K nearest neighbor. 


#Conculsion
It is also noteworthy that it is common to use classification accuracy as a first measure to judge classifier performance, but when the classes are as imbalanced as in the case of credit card data, accuracy measures are misleading because they may just reflect the underlying class distribution even if the true accuracy is higher. It is better to consider sensitivity (recall) and specificity that give more insight into the classifier performance.

For instance, if the true fraud credit card transaction is classified as false, then is is a huge loss for banks and customers. However, if the true transaction was classified as fraud, eventhough it is not favorable, atleast banks won't lose money. Therefore, more weightage should be given to detect fraud transaction as fraud i.e True positives with higher accuracy i.e. higher recall/sensitivity is favorable.

In our test on different classifiers with Random forest, logistic regression and Naive Bayes Classifier, we found logisistic regression to be performing better than other two with higher recall= 95% on test set.
