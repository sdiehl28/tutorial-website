---
title: "Categorical Encoding"
description: ""
weight: 40
alwaysopen: false
lastmod: 2018-05-01
typora-root-url: /home/agni/SoftwareProjects/Sites/tutorial/static/
---
#### Notebook: <a href="http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/Titanic04.ipynb" target="_blank">Categorical Encoding</a>
#### Goals  
* Discuss Categorical Encoding
* Demonstrate One Hot Encoding
* As part of iterative model development, check if one hot encoded categorical variables improved the model's accuracy.

#### Results  
* Demonstrated one hot encoding for Sex and Embarked
* Measured the new model's accuracy and found it was much better (80.0% vs 70.9%).

The following boxplot shows the 10 cross validated scores for this iteration and the previous iteration.
<img src='/images/4_vs_3.png'>

The scores were slightly improved.  Encoding the Sex and Embarked variables as dummy variables and then including these features in the model, allowed for a significantly better model.

#### Next

Now that all the variables that are "easy" to make use of, have been used.  The possible extracted features noted in the [first iteration](/projects/titanic/titanic01) will be tried.
