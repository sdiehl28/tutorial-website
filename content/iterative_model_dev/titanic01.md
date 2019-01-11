---
title: "Create Baseline Model"
description: ""
weight: 30
alwaysopen: false
lastmod: 2018-04-29
typora-root-url: /home/agni/SoftwareProjects/Sites/tutorial/static/
---

#### Notebook:  <a href="http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/Titanic01.ipynb" target="_blank">Create Baseline Model</a>
#### Goals
* Perform Exploratory Data Analysis
* Create simple baseline model
* Measure performance using cross validation
* Compare baseline model with null model

<div class="alert alert-success">
<strong>Tip:</strong> The Jupyter Notebook link above provides the discussion and code.  This web page is just a minimal summary.
</div>

#### Results
In this first iteration we:

- performed EDA
- preprocessed data in a simple way
- created a simple LogisticRegression model
- created a null model (aka DummyClassifier) for comparison
- used cross validation to measure the accuracy of each model
- discussed StratifiedKFold and KFold for use with cross validation

The following is a boxplot of the base model and the null mode using 10 cross validated accuracy scores.

<img src='/images/base_vs_null.png'>

The base model had an mean cross validated accuracy of 68.7%.  The null model had a mean cross validated accuracy of 61.6%.

The base model is significantly better than the null model.

For a discussion on how to compare models based on cross validated scores, see my post: [Model Selection](/posts/model_comparison/)

#### Next

Improve the model by replacing missing Age values with the mean Age value and use the Age variable in the model.
