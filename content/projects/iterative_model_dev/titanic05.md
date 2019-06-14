---
title: Encapsulating Data Processing with Pipes
weight: 70
alwaysopen: false
lastmod: 2019-06-14
typora-root-url: ../../../static
---
#### Notebook: <a href="http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/TitanicN05.ipynb" target="_blank">Encapsulating Data Processing with Pipes</a>
#### Goals  
* Use all numeric features
* Standardize and impute missing values
* Use new v0.21 IterativeImputer

#### Results  
The following boxplot shows the cross validated scores for this iteration and the previous iteration.  <img src='/images/2_vs_1.png'>

The new model, using all the numeric features along with standardization and imputation, is better.

#### Next

Encapsulate Data Processing with ColumnTransformer.
