---
title: Encapsulating Data Processing with ColumnTransformer
weight: 80
alwaysopen: false
lastmod: 2019-06-14
typora-root-url: ../../../static
---
#### Notebook: <a href="http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/TitanicN06.ipynb" target="_blank">Encapsulating Data Processing with ColumnTransformer</a>
#### Goals  
* Use v0.20 ColumnTransformer to allow a Pipeline per Feature
* Use Extracted Numeric Features suggested by EDA
* Encapsulate Feature Encoding and Feature Transformation in Functions
  * get_Xy -- will get encoded data
  * get_ct -- will get feature transformer to be used on encoded data
* More discussion on Data Leakage

#### Results  
The following boxplot shows the cross validated scores for this iteration and the previous iteration.  <img src='/images/3_vs_2.png'>

The scores improved.  Using the new features helped.

#### Next

Categorical Encoding.