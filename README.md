# Class 12.1

# Classification and Natural Langauge Processing 
November 28, 2020

## Classification Review

Today's class began with a review of classification. Classification falls under the supervised learning branch of Machine Learning. Mia began the review with how classification is different from regression. First, classification algorithms produce a discrete variable whereas regression algos produce a continuous variable. Second, classification produces a decision boundary that literally classifies the two groups of data. Regression, by contrast, produces a 'best fit line'. Classification models are: KNN, Decision Trees, Logistic Regression, Random Forest, Naive Bayes and SVM (Support Vector Machine). Regression algos, by contrast, are: linear/polynomial/multi-linear regression, Decision Tree, RF and Neural Networks. Any business case that requires optimization will use a regression algorithm. Any business case that requires a grouping process will use a clustering algorithm. 

**Random Forest/Decision Tree based algos**

Classical Decision Trees are a sequence of if, else statments. Decision Trees can be very deep and are not so useful when dealing with imbalanced data sets. Random Forests, however, are useful because they are comprised of multiple small, simple Decision Trees. They are built to categrorize small segments of a data set and are an example of how weak learners are combined into an ensemble to produce highly statistically significant classification results. In Random Forests, the entire data set is not analysed whereas in a classical Decision Tree, it is. Random Forests are faster, very robust and typically result in less over fitting. 

**Bayes' Theorem** is an algo that judges if an event will occur. 

**SVM** 

Support Vector Machines is an algorithm that maximizes the difference between clustered groups. The points farthest from the mean of a clustered group are used as vector placement in what is called the hyper plane. There are multiple kernel types to transform data into high dimensional space and they are: poly, radial bases function 'rbf', sigmoid, linear and non-linear. It is also imporant to understand the data set prior to choosing which kernel to use in SVM.

The accuracy score of a classification algorithm can be misleading if working with imbalanced data sets. Therefore, it is imperative to check the Recall, Percision and F1 scores. 

**Data Prepocessing**

Data must be preprocessed before being fed into an algorithm and the two steps to cleaning the data are: Standard Scaler and Binary Encoding. Standard scalar standardizes all the numeric values prior to the algorithm. The next step is to convert all the alpha numeric values into binary via pd.get_dummies().

**Bagging & Boosting** 

Why use bagging/boosting/gradient boosting algorithms?
- They work well with imbalanced data sets
- They work well with highly complex/multi variable data sets
- They are more accurate than the simpler algorithms

Steps that allow us to increase an algorithm's speed are: feature importance and learning rate. If working on a classification porblem, one should start with random forest, then SVM and then finally use a bagging/boosting algorithm. 

**Imabalanced Data Sets** 

When working with imbalanced data sets, the model has to learn from minority classes in addition to majority classes in order to be able to generalize in a new data set. Some potential strategies for dealing with imbalanced data are the following: Oversampling/undersampling/Combined Sampling, correct performance metrics or a change in model. The theory is that algorithms, with their specific functions, coupled with oversampling the minority or undersampling the majority classes will achieve a more balanced outcome. 

Oversampling works via SMOTE (Synthetic Minority Oversampling Technique) which adds additional samples of minority data until the minority data = majority data. Undersampling is the process of undersampling majority data until majority data = minority data. Typically however, both techniques are used together via SMOTEENN. It first overamples the minority then undersamples the majority to create a balanced output. Undersampling, however, is no good when the data set is small. 

---
## Introduction to Natural Language Processing

Natural language processing (NLP) is the branch of AI that processes written and spoken language to then be fed into the computer for algorithms such as sentiment analysis. NLP is used heavily in legal AI to automate the reviewal process of thousands of documents for case analysis. 

NLP is used in finance to automate sentiment analysis of earnings statements and investor cells to predict future value etc. 

NLP's workflow is slightly different than the model, fit, predict workflow in Machine Learning. It is: preprocessing, extraction, analysis and representation. 

Features of NLP preprocessing are tokenization, stop words, and lemmatization. Tokenization is the process of splitting up a text document into units. Stop words are words that for the purpose of analysis are removed, example: the, this, to etc. Lemmatization standardizes the morphology of words. For example, walking, walked, walks become walk via lemmatization. 