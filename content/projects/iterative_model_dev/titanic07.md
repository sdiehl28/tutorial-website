---
title: Categorical Encoding
weight: 90
alwaysopen: false
lastmod: 2019-06-14
typora-root-url: ../../../static
---
#### Notebook: <a href="http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/TitanicN07.ipynb" target="_blank">Encapsulating Data Processing with ColumnTransformer</a>
#### Goals  
* Use Extracted Categorical Features suggested by EDA
* Encode Categorical Features
* Refine Feature Encoding and Feature Transformation Functions
* Simplify Model

#### Results  
The following boxplot shows the cross validated scores for this iteration and the previous iteration.  <img src='/images/4_vs_3.png'>

The scores slightly improved.  Using the new features helped.

Basic model building is complete.  

All features available, as well as extracted features suggested by the initial EDA, were tried.  Several of the extracted features were then removed, and the model was found to do just as well.  All else being equal, a simpler model is preferred over a more complex model having the same performance.  The simpler set of features will be used going forward.

#### Next

Hyperparameter Optimization
