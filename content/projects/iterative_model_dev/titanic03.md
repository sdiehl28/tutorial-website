---
title: First Model
weight: 50
alwaysopen: false
lastmod: 2019-06-13
typora-root-url: ../../../static
---
#### Notebook: <a href="http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/TitanicN03.ipynb" target="_blank">Create First Model</a>

#### Goals  
* Begin with most promising features found during EDA
* Begin with simple or no preprocessing.
* Compare with Null Model

#### Results
This iteration used Pclass and Sex with no data transformations.

The following boxplot shows the cross validated scores for this iteration and compares it with the null model.
![1_vs_0](/images/1_vs_0.png)

The base model's accuracy is much higher than the null model (which always predicts NotSurvived).

#### Next

Discuss Cross Validation and Avoiding Data Leakage.