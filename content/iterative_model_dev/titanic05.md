+++
title = "Feature Extraction"
description = ""
weight = 70
alwaysopen = false
lastmod = 2018-05-08
typora-root-url = "/home/agni/SoftwareProjects/Sites/tutorial/static/"
+++
#### Notebook: <a href="http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/Titanic05.ipynb" target="_blank">Feature Extraction</a>
#### Goals  
* In the first iteration of model building, several feature extraction ideas were presented. See: EDA
* Implement these.
* As part of iterative model development, compare performance with previous iterations.

#### Results  
- Added the features suggested in the first iteration of model building
- Measured the new model's accuracy and found it to be slightly better (81.6% vs 80.0%)

The following boxplot shows the 10 cross validated scores for this iteration and the previous iteration.  <img src='/images/5_vs_4.png'>

The scores slightly improved.  Using the new features helped.

#### Next

Now that the LogisticRegression model is looking good, let's try another model, XGBoost, using the same features.  This will bring up the topic of HyperParameter Tuning.

#### The next notebook has not yet been written.