+++
title = "Model Selection"
description = ""
weight = 30
lastmod = 2018-04-27
+++
Some of the material for this post comes from my understanding of the following:

* [Statistical Comparisons of Classifiers over Multiple Data Sets](http://www.jmlr.org/papers/v7/demsar06a.html)
* [An Introduction to Statistical Learning](http://www-bcf.usc.edu/~gareth/ISL/)

### Model Selection Problem

A model is changed and we would like to see if it has higher "accuracy".  Here I will use "accuracy" as a generic term for any performance metric of interest that we wish to improve.

### Cross Validation Setup

The cross validation scores for the models being compared should be made over the same train/test splits.  This can be done by using the same random_state parameter for each.

### Model Selection Scenarios

Suppose we compute the mean score of the cross validation scores and it is slightly better than the previous version.  How do we know if it really is better, or it is just better by chance due to noise in the measured scores?

We could measure the variance of each set of cross validated scores as a measure of inherent "noise".  We could compare the means of the two sets of cross validated scores and see if the difference in the means is above some measure of the noise, and if so, declare that the new model has a "statistically significant" difference.

Before diving into this further, it is helpful to step back and consider the big picture.  We are considering choosing one model over another, but what is the context?

**Scenario 1**

We have a prediction model running in production.  We are considering making a change that will cost time and money to implement.  We would like some assurance that the new model is not just barely better than the old model, but rather that the extra revenue we get from the new model being more accurate more than offsets the cost to implement it.  That is, we are looking for "practical significance" and this requires a cost/benefit analysis.

**Scenario 2**

We are publishing an academic paper or writing a blog post.  If we see a statistically significant difference, we would like to explore why the latest model change resulted in an improvement.

**Scenario 3**

A submodule of our prediction system is running code that automatically picks the best version of the model based on the best score.  The automated submodule needs to pick a model in order to continue.  If both models are effectively the same, then it doesn't matter which model gets chosen by selecting the mode with the best score.

**Summary**

Deciding which is the "best" model to pick depends upon your use of that model.  There is no one way to define "best".

It is also worthwhile to consider Occam's razor: given two equivalent choices we prefer the simpler of the two.  This choice often leads to models that generalize better on new data.

#### Cross Validation

Cross validation can be used to:

- estimate the performance of a model
- compare two different models
- compare the same model having different hyper parameters

Cross Validation may introduce a bias into the point-estimate of a model's accuracy, but if this bias is similar for all the models under consideration, this bias does not matter.  Model comparison is effectively subtracting one model's scores from another, and if both are biased in similar ways, the bias cancels outs.  This makes cross validation excellent for model comparison.

If only one model is being considered, we need to be more cautious.  There may be no better way to estimate how it will perform on out-of-sample data, but it may not be as accurate as the spread of the cross validated scores suggest.

#### Repeated Cross Validation

The idea behind repeated cross validation is that by repeating the entire cross validation process (using different train/test splits) we acquire more estimates of the model's scores.  And if these additional estimates are independent then we could, for example, average them to create a better point-estimate of the model's score.  However the estimates are not independent.  Cross Validation, and to an even greater extent, Repeated Cross Validation, uses overlapping data sets.  Overlapping data is, by definition, not independent.

There doesn't seem to be a general consensus yet as to whether or not repeated cross validation improves the point-estimate of the model's score.  It almost certainly does not improve the variance estimate of the model's score as this is strongly affected by non-independent data.

#### Statistical Significance

A key assumption for most statistical tests of significance is independent data.  Cross Validation is based on overlapping data sets which are not independent.

The most obvious statistical test to compare two sets of cross validated scores is the paired t-test.  It is paired because we have scores that were computed over the same train/test splits.  However given that the assumption of independence is violated, this renders the paired t-test almost meaningless.  That said, there are data scientists who use it, or uses it with "5x2CV" (2-fold cross validation repeated 5 times followed by a paired t-test), but the general feeling appears to be that the assumptions of the paired t-test are violated, therefore the paired t-test should not be used.

A non-parametric test similar to the paired t-test is the Wilcoxon Rank Sum Test.  This test makes fewer assumptions about the underlying data.  Common sense says we could use this test, as one tool in our tool box, to help us decide which model to chose but relying on it exclusively is probably not a good idea.

For a very large data set, Cross Validation is unnecessary.  The models could be built on two or more non-overlapping training sets and evaluated on one or more test sets.  If the models being compared are trained on the same training sets,  and evaluated on the same test sets, then it may make sense to use the Wilcoxon Rank Sum test.

#### Other Tools for Model Selection

Given that each model is being compared on the same train/test split, we can subtract the scores of one model from the other and look at the differences.  We could display a box plot of these differences.  This would provide a visual overview of how the model's compare to one another.

We could informally decide that if one model does better than another most of the time, then this is the better model.  However we cannot formalize this with, for example a binomial test of the number of "wins/losses", as the assumption of independent data is not met.

In *Introduction to Statistical Learning*, when they are considering the validation curve of model performance on the test set vs model complexity, they suggest using the simplest model that is within one standard deviation of the best test score.  This heuristic says that simpler is better, up to (an estimated) 1 standard deviation's worth of performance.  Given that the authors are experts in their field, this seems like an excellent technique for combining Occam's Razor with estimated model performance.

### Model Selection Criteria Used for this Website

The models being compared will be run with the same random_state.  This makes the cross validation scores directly comparable.

In most cases, displaying a boxplot of each model's cross validated scores is enough to determine by eye which model is better.  However if the model's performance is close, I will subtract the corresponding scores from each other and create a boxplot of the differences.  I will also compute a "win/tie/loss" count for comparison.