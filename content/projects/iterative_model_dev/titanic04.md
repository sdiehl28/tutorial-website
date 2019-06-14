---
title: CV and Avoiding Data Leakage
weight: 60
alwaysopen: false
lastmod: 2019-06-14
typora-root-url: ../../../static
---
#### Notebook: <a href="http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/TitanicN04.ipynb" target="_blank">Cross Validation and Avoiding Data Leakage</a>
#### Goals  
* Data Leakage: Test data leaking into the model building process should be avoided.
  * Never use the test set's target variable as part of the model building process
  * Never use any of the test set data as part of the model building process -- better
* Demonstrate that Feature Transformations, with and without Data Leakage, have different results.

#### Next

Encapsulating Data Processing with Pipes
