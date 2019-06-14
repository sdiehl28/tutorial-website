---
title: Hyperparameter Optimization
weight: 100
alwaysopen: false
lastmod: 2019-06-14
typora-root-url: ../../../static
---
#### Notebook: <a href="http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/TitanicN08.ipynb" target="_blank">Hyperparameter Optimization</a>
#### Goals  
- Optimize the hyperparameter for regularization
- One Standard Error Rule
- Specialized Learning Curve to find Best K for Model Ranking
- Nested Cross Validation

#### Results  

Selecting the value for C that is one standard error less than the optimum found with GridSearchCV.

![one-standard-error-curve](/images/ScoreVsRegularization.png)

Customized Learning Curve which shows K=2 is best for model ranking and K=5 is best for model evaluation, for K-Fold Cross Validation.

![ScoreVsK](/images/ScoreVsK.png)

The optimized version of the model did not perform any better than the out-of-the-box LogisticRegression model.  The Titanic data set is too small and simple to benefit from more advanced techniques.  In the last notebook of this series, a simple decision tree will be created which predicts well and shows how simple this data set is.

#### Next

Ensembles.
