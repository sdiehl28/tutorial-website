---
title: Model Building
weight: 30
alwaysopen: false
lastmod: 2019-06-12
typora-root-url: ../../../static
---
#### Notebook:  <a href="http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/TitanicN01.ipynb" target="_blank">Model Building</a>
#### Goals
- Iterative Model Building
- Ranking vs Evaluating Models

<div class="alert alert-success">
<strong>Tip:</strong> The Jupyter Notebook link at the top of each web page provides the full discussion and code.  Each web page only provides a minimal summary.
</div>

#### Iterative Model Building

At the highest level, the Model Development Process is:

- create a baseline model
- iteratively improve upon that model

Improvement means:

- improve model accuracy or interpretability
- improve software workflow

The benefits of improved software workflow include:

- reproducibility
- experimental flexibility
- reduced software and model evaluation bugs

#### Ranking vs Evaluating Models

As per the discussion in the notebook for K-Fold Cross Validation, it was suggested that:

1. For an absolute model score: use K=5 or K=10
2. For a relative model score: use K=2 or K=3

Furthermore, repeating cross validation 10 times lowers the variance of the score.

A Learning Curve can be created which uses K on the x-axis instead of the number of records.  Higher K means more records to train on.  The error bars represent one standard deviation above and below the mean cross validated score.

![1_vs_0](/images/ScoreVsK.png)

From the above, K=2 is best for ranking models and K=5 is best for evaluating models on this dataset.

#### Next

Use Seaborn to perform Exploratory Data Analysis.
