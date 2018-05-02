---
title: "Cross Validation"
description:  ""
weight: 20
alwaysopen: false
lastmod: 2018-05-01
typora-root-url: /home/agni/SoftwareProjects/Sites/tutorial/static/
---
#### Notebook: <a href="http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/Titanic02.ipynb" target="_blank">Cross Validation</a>
#### Goals  
* Add Age to the model (requires imputation of missing values)
* Demonstrate the right and wrong way to perform Cross Validation
* Compare this model with the previous iteration

<div class="alert alert-success">
<strong>Tip:</strong> The Jupyter Notebook link above provides the discussion and code.  This web page is just a minimal summary.
</div>

#### Results  

* Added Age to the model
* Imputed the missing Age values
* Showed the right and wrong way to setup for cross validation
* Used Imputation as part of a Pipeline, along with cross_val_score.

This iteration adds Age to the model.

The folowing boxplot shows the 10 cross validated scores for this iteration and the previous iteration.

<img src='/images/2_vs_1.png'>

The base model had an mean cross validated accuracy of 68.7%.  The new model has a mean cross validated accuracy of 70.2%.

The new model is very slightly better.

For a discussion on how to compare models based on cross validated scores, see my post: [Model Selection](/posts/model_comparison/)

#### Next

For the next iteration, we will perform a better imputation of the missing Age value by using groups.