---
title: "Create Baseline Model"
description: ""
weight: 10
alwaysopen: false
lastmod: 2018-04-29
typora-root-url: /home/agni/SoftwareProjects/Sites/tutorial/static/
---
#### Jupyter Notebook: <a href="http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/Titanic01.ipynb" target="_blank">Create Baseline Model</a>
### Notebook Goals
* Create simple baseline model
* Perform Exploratory Data Analysis
* Demonstrate details of Scikit Learn's:
  * KFold
  * StratifiedKFold (with shuffle=True and shuffle=False)
  * cross_val_score
* Measure baseline model's score and compare against null model

<div class="alert alert-success">
<strong>Tip:</strong> The Jupyter Notebook link above provides the discussion and code.  This web page is just a minimal summary.
</div>

### Notebook Results  
* Data was preprocessed in a simple way
* LogisticRegression model was created
* Null model (aka DummyClassifier) was created
* Both models were scored by accuracy using 10 fold cross validation (CV) with the same random_state.
* How Scikit Learn implements CV with StratifiedKFold (shuffle=True) and cross_val_score was discussed

The base model demonstrates a simple use of LogisticRegression.

The null model predicts the predominant class for every prediction.

The following is a boxplot of the 10 cross validated accuracy scores.

<img src='/images/base_vs_null.png'>

The base model had an mean cross validated accuracy of 68.7%.  The null model had a mean cross validated accuracy of 61.6%.

The base model is significantly better than the null model.

For a discussion on how to compare models based on cross validated scores, see my post: [Model Selection](/posts/model_comparison/)

#### Next

Improve the model by replacing missing Age values with the mean Age value and use the Age variable in the model.
