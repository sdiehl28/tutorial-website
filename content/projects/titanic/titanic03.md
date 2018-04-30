---
title: "Custom Transformers"
description: ""
weight: 30
alwaysopen: false
lastmod: 2018-04-29
typora-root-url: /home/agni/SoftwareProjects/Sites/tutorial/static/
---
#### Jupyter Notebook: <a href="http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/Titanic03.ipynb" target="_blank">Custom Transformers</a>

### Notebook Goals  
* Perform better Age imputation
* To avoid data leakage, this requires creating a custom Transform class. Demonstrate this
* Understand Panda's GroupBy in detail for use in the custom Transform class
* As part of iterative model development, check if this improves the model's accuracy

### Notebook Results
* showed how to create a custom Transform object to perform custom Imputation
* examined the GroupBy objects in detail
* performed custom Age Imputation without data leakage

This iteration uses custom Age imputation to better replace missing Age values based on the values of (Pclass, Sex).

The folowing boxplot shows the 10 cross validated scores for this iteration and the previous iteration.
<img src='/images/3_vs_2.png'>

The new model's mean accuracy is 70.9% which is slightly better than the previous iteration of 70.2%.

#### Next

For the next iteration, we will use one-hot encoding to make direct use of two more variables, Sex and Embarked.