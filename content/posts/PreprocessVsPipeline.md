---
title: "Preprocess vs Pipeline"
description: ""
weight: 40
alwaysopen: true
draft: true
lastmod: 2018-05-08
typora-root-url: /home/agni/SoftwareProjects/Sites/tutorial/static/
---

The issue is how to avoid data leakage.

1. What types of preprocessing can be performed on the entire dataset, prior to model building?
2. What types of preprocessing must be part of the model building process itself, in order to ensure that the model generalizes well?

Any process which does not depend on the values of the data, can be performed prior to model building.  

Some examples:
- exclude features due to time constraints
  - if you need to quickly build a model, you could chose which features to use based on which require the least amount of your time to use appropriately.
- changing data representation, such as representing a categorical variable as in integer or a series of dummy values
  - it is okay to look at the data to find the distinct possible values for a categorical variable and perform an encoding based on those distinct values
  - it is not okay to use an encoding which makes use of the observed distribution of the categorical values (unless that distribution is fixed by the domain)
  - 
  - , would be based on the data, and would need to be part of a pipeline
- removing collinear variables
- performing principal component analysis or k-means clustering
- feature extraction

It might seem that removing collinear variables is "looking at the data", but it isn't really.  Any variable that is a linear combination of other variables is a redundant variable.  Some algorithms, such as linear regression and logistic regression do not work will if there are redundant variables.  Removing a redundant variable is not "looking at its values".

Some of the above seem gray area.  Doesn't PCA or collinearity depend upon the values of the data?  It does, but the information content of the data is not changed.  alternative representation.  Removing duplicated variables.


Any process which depends upon the values of the data, must be part of the model building process.  In most cases, this means putting them in a pipeline.

Some examples:
1. impute missing values with mean
2. normalize the data
3. select variables based on some statistic of the data, such as "most important via RandomForest"



It is necessary to quantify how to measure how "good" a model is.  We need to define how good a model is in order to:
1. select the best model
2. optimize hyperparameters for  given model

The value of a model's predictions depends upon the context in which it is used.  This "value" is qualitatively accessed in a business set


A "model" is a mapping from feature space to target space.

A "good" model must be one that predicts well on unseen data.  Any model can memorize data its been given and "predict" from memory, but only a useful

A "good" model can be defined in many ways, therefore there are 


How good a model is depends upon the context in which it is used.

It is helpful to quantitatively define the concept of model "goodness".  This is done by formally defining a metric.  A metric is a specific way to measure, such as accuracy or area-under-the-curve or log-loss.


It is helpful to quantitatively define the concept of model "goodness".  This is done by defining a "metric". A metric is specific way to measure.  For classification, "accuracy" is one metric.  It is the total number of correct predictions divded by the total number of predictions.  If the benefit of a correct prediction equals the loss of an incorrect prediction, the "accuracy" can be a good metric to use.  Another metric is "recall", which is defined to be the number of correct positive prediction divided by the total number of positive predictions.

It is helpful to quantitatively define the concept of model "goodness".

how "good" a model is.  How good a model is depends upon the context in which it is used.


of a "good" model. 


For the sake of this explanation, "model performance" means "model accuracy" which means how well a model predicts.

A "metric" is a specific way to measure. There are multiple ways to measure how "good" a model is.  For classification, accuracy is the simplest such measure.

For example, accuracy for a classification problem is one metric.  "Recall" for classification is another metric.  When trying to predict a rare event, such as cancer, the more appropriate measure is recall.

Another might be "recall" predicting a rare value.

There are many metrics that exist for measuring how well a model predicts, most of which convey some sort of 

but most of them have the general meaning of "accuracy".

which means how well does the model predict.


A train/test split or cross validation is used to compute

an accurate estimate of a model's performance.

For concreteness, let's say that performance means accuracy of prediction.  There are many measures of performance possible, but accuracy conveys the general meaning of all of them.


Using a train/test split or cross validation, has one many affect, 

Using a train/test split or cross validation, allows a good estimate of the model performance to be computed


There are two key reasons for using a train/test split or cross validation:
* model performance evaluation
* overfitting

Techniques such as using a train/test split, or a generalization of that, cross validatin

The key idea for model evaluation, and model building with automated parameter tuning, 

A model is built on training data and tested on test (held-out) data.  This assures that the model was not overfit to the training data.  When a model is overit, it means the model was fitted to the noise in the training data. The noise in the training data, being random, will not be the same on other data sets.  Testing the performance of the model on test data gives a better idea on how the model will generally perform on new data.



In the simplest case, a model is built on training data and it is tested on test (held-out) data.  What preprocessing operations can be performed prior to the model building process?

Certainly anything having to do with acquiring the data, performing joins on the data, using domain knowledge to exclude certain columns (without looking at the values in those or other columns) are all cases in which the preprocessing.

colinearity can be removed

columns based on correlation cannot

Some preprocessing steps do not require looking at the values in the data, as such, 

Any step that essential to the model building process itself, should be applied to the training data separately from the test data.

For example, deciding which columns to use based on a statistic computed from the data, 

A model is built on training data, and i


What types of preprocessing can take place before the model building process and what types must be part of the model building process?  The answer is not always clear cut.

Representing a categorical variable having 5 distinct values using dummy variables, could be performed prior to starting the model building process.

On the other hand, using the distribution of categorical values to create an encoding, is not as clear cut.  If domain knowledge said that the observed distribution is likely to remain the same, then this encoding could occur prior to the model building process.

When can a transformation take place without causing data leakage?  The answer is not always clear cut.

Representing a categorical variable as dummy variables can take place propr 

Encoding a categorical variable as a number, if its only based on distinct values, can take place prior to the model building process.  On the other hand, creating an encoding on the fly based on the frequency of categorical values, 


If a variable transformation depends on the values in the dataset, then this transform operation should be part of a pipeline to avoid data leakage.  See previous notebooks [CV Right and Wrong](http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/Titanic02.ipynb#crossvalidation) and [Data Leakage](http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/Titanic02.ipynb#dataleakage)

As per the first iteration's EDA notes, the full set of transformations to try is:
1. Extract binary categorical feature: alone
2. Extract ordered categorical feature: fare
3. One Hot Encode unordered categorical features
4. Impute Age as per previous iteration's custom transform class
5. Standardize all numeric features
6. Compute Cross Validated Model Scores 



It is okay to represent the same information in a different way without maki

When can a transformation be run prior to model building, and when must it be part of a pipeline for cross validated scoring?

If the transformation changes the information content of the data, such as dropping columns based on a statistic, or 

Manually extracting a few features, based on domain knowledge or EDA of a subset of the data, can probably be safely performed prior to model building.  

take place as part of preprocessing, with the model built afterwards, and when should a transformation be part of a pipeline for cross validation scoring?

Of course, if there is so much data that cross validation is not necessary, then 
The question in preprocessing is, when can a transformation be performed up front, on all the data, with the model built afterwards, vs when should the transformation be part of a pipeline for cross validation so that data leakage doest not occur.

One way to look at it is, if the information content of the transformed data is the same, then the transformation need not be part of pipeline.  

Changing the representation of a variable, such as using one hot encoding, can be done up front, before model building.  This is because the information content of that categorical value is not used in the transformation; only its distinct values are.  Now if the distribution of the categorical values was part of the transformation, then that transformation probably should be in a pipeline.

It is not always clear cut as to whether or not data leakage is enough of an issue to warrant extra code.  Changing the representation of a variable, such as using one hot encoding, need not be performed in a pipeline.  The information content of that variable is not used as part of the transformation, only it's distinct values are.

Sometimes there is a gray area with respect to data leakage.  Creating a new feature probably doesn't require using a pipeline.  Automatically generating many new features to try, probably would.  Dummy encoding can occur before model building.

Extracting a couple of features is
Arguably, creating a couple of features does not

A preprocessing operation which changes the representation of data doesn't require using a pipeline (unless there are so many different representation
A preprocessing operation which changes the representation of the data, but does not change the information represented, can be performed without a pipeline.

Preprocessing operations which do not use the data in order to change the information represented, 