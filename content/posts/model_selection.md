---
title: "Model Selection"
description: ""
weight: 30
draft: false
lastmod: 2018-05-14
typora-root-url: /home/agni/SoftwareProjects/Sites/tutorial/static/
---
The following papers greatly influenced this post and I would recommend reading them.  This post attempts to present a simple summary of these ideas.

* [On over-fitting in model selection and subsequent selection bias in performance evaluation](http://www.jmlr.org/papers/volume11/cawley10a/cawley10a.pdf)

#### Terminology

For this post, I use the following terms.

"CV" means Cross Validation.  It is used to estimate the performance of the model on data it was not trained on.

"Model" means a specific model built from a specific dataset.

"Model Selection" means to choose the best model based on its score.  The score could be computed from any of the scorers in sklearn.metrics, or it could be a customer scorer.

"Model Parameters" are the parameters of a model which are determined by fitting the model to the data. For example, the linear regression coefficients for each feature and the intercept.

"Model Hyperparameters" are those parameters which are not determined by fitting the model to the data, but are part of the model definition. For example, the amount of regularization, alpha, for the Lasso is a hyperparameter.

Scikit Learn offers some methods which determine both the parameters and the hyperparameters, such as sklearn.LinearModel.LassoCV.  This method is offered because there is an efficient way to find both alpha and the linear coefficients.  In other words, LassoCV is more efficient than using GridSearchCV with the Lasso.  Nevertheless, the CV at the end of the estimator name is a give-away that internally it is performing cross validation and the reason that it is performing cross validation is to find the best hyperparameter.

Minimize a loss function is maximize an objective function.



#### Statistical Approach

We could try to formalize this with statistics, but the model evaluation data we have is usually in the form of cross validated scores.  Cross validated scores are the result of building models on overlapping data.  Overlapping data is not independent, so most statistical tests will not provide accurate results.

Occasionally statistical tests are used, such as "5x2CV", which is 2-fold cross validation repeated 5 times followed by a paired t-test.  But as the data is not independent, it's hard to say how much value this test provides.

If there is enough data that Cross Validation isn't necessary; for example, building models using non-overlapping subsets of the data for training and evaluating these models on non-overlapping subsets of the data for testing, then as per [Statistical Comparisons of Classifiers over Multiple Data Sets](http://www.jmlr.org/papers/v7/demsar06a.html) a statistical test such as the Wilcox Rank Sum test could be used.

#### Informal Approach

Usually a less formal comparison is performed, such as displaying a boxplot of the cross validated scores.  If the models being compared were run with the same random_state parameter, producing the same train/test splits, then the cross validated scores can be compared by eye with a box plot.  If the model's performance is close, it may be helpful to subtract the corresponding scores from each other and display a boxplot of the differences, or tally up the "wins/ties/losses" per train/test split, to get a better sense of which model may be best.

#### Comparing Scores

It is worthwhile to consider Occam's razor: given two equivalent choices we prefer the simpler of the two.  Choosing the simpler model, often leads to models that generalize better on new data.

In [An Introduction to Statistical Learning](http://www-bcf.usc.edu/~gareth/ISL/) they propose a heuristic, in conjunction with the validation curve which plots test set performance vs model complexity, that choosing the simplest model within one standard deviation of the best model's score is a good choice.  The idea being that two models differing by one standard deviation are essentially equivalent, so pick the simpler of the two.

Although "standard deviation" is easy to define and calculate on a set of cross validated scores, the distribution of the cross validated scores is not normal (and is not known) as the data it is derived from is not independent.  This means the actual confidence interval will be larger than that computed assuming a normal (or t) distribution. 

Cross Validation may introduce a bias in the point-estimate of a model's accuracy, but it's likely this bias is similar for both model's under consideration.  This means that the bias does not affect the determination of which model is best.  This also means that using the cross validated score for a single model about to be deployed to a production environment is somewhat risky.  There could be bias in the point-estimate.  And if a confidence interval about that point-estimate is computed assuming that the cross validated scores are normally (or t) distributed, than that confidence interval would be too narrow (for the specified probability level).

The standard deviation of the cross validated scores is likely useful as a relative measure of variance.  For example, given two models with about the same mean cross validated score, but one has a much higher standard deviation than the other, the "best" model would likely be the one with the lower standard deviation.

#### Cost to Deploy

There may be a cost associated with deploying a new model.  If we have a proposed model that is more accurate than a model already running in production, we need to compare an estimate of the cost to deploy the new model relative to an estimate of the profit the new model will provide, in order to decide what to do.

Or there my be no cost associated with deploying a new model.  If we have a submodule of our prediction system that just needs to pick the "best" model in order to move forward, having code which automatically choose the "best" model based on mean CV score may be fine.

#### Repeated Cross Validation

Repeated cross validation, which is repeating the cross validation process a number of times with different train/test splits, may not improve the point-estimate of the model's score or narrow it's variance estimate because it is using even more overlapping data than regular cross validation.  In general, it may be best to avoid this technique unless you have a specific reason for using it.

### Summary

For this website, I will use an informal comparison of cross validated scores displayed as boxplots.  If the model's performance is close, I will subtract the corresponding scores from each other and display that as a boxplot, as well as computing a "wins/ties/losses" tally to get a sense for which model may be best.