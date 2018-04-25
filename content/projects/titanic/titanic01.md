+++
title = "Establish Baseline Model"
description = ""
weight = 10
alwaysopen = false
lastmod = 2018-03-06
+++

### Establish Baseline Model

Jupyter Notebook: [Baseline Model](http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/Titanic01.ipynb)

The first iteration is about:

* quickly getting a model working
* establishing a baseline level of accuracy

Quickly getting a model working is analogous to the software engineering concept of creating a [skeleton](https://en.wikipedia.org/wiki/Skeleton_(computer_programming)).

Once you have a model running, you can gradually improve it by repeatedly iterating over each step.

Improvement is something that should be measured. For a predictive model, the model's accuracy is a simple measure of its value.

As you strive to continually improve your model's accuracy, you should keep a record of what you did, both the successes and failures. Understanding what steps improve your model can provide valuable insights into how your input variables relate to your prediction.

Keeping track of how you built your model is part of [Repeatable Research](https://en.wikipedia.org/wiki/Reproducibility).

Repeatability is key to allowing yourself and others to check your work for subtle errors, such as leakage from the test data into the model building process, and for clues on how to improve the model further.

### Evaluate Model Performance

The Jupyter Notebook discussed both train/test split and cross validation as method to estimate the model's performance on out-of-sample data.