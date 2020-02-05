+++
title = "Table of Contents"
description = ""
weight = 10
alwaysopen = false
head = "<label>Jupyter Notebooks</label>"
lastmod = 2020-02-05

+++

Here is a list of the Jupyter Notebooks I have created on github, organized by topic.

These notebooks are designed for use with jupyter lab and the Table of Contents extension: [JupyterLab TOC Extension](https://github.com/jupyterlab/jupyterlab-toc) or with jupyter notebook.

### Python Programming

A basic understanding of Python and programming is assumed.  Some commonly misunderstood examples are presented.

* [Core Python 1](
  http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/CorePython.ipynb)
  * floating point equality
  * 'is' vs '=='
  *  mutable vs immutable (several visual examples)
* [Core Python 2](
  http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/CorePython2.ipynb)
  * str vs repr
  * string formatting
  * recursion example
  * use key with max and sorted
  * Python 3.6 NamedTuple
  * Python 3.6 dataclasses
  * dict with value being list
  * iterator and iterable
  * closures

### Regular Expressions

* [RegEx: Examples]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/RegEx.ipynb)
  * re.search()
  * search flags
  * Python raw strings
  * quantifiers
  * re.finditer()
  * greedy vs non-greedy matching
  * **\b** (anchor) vs **\s** (whitespace)
  * character ranges
  * order of matching when using alternatives
  * metacharacters
  * groups
  * matching across lines
  * lookahead and lookbehind
* [RegEx: Parse Jupyter NB]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/RegExParseNB.ipynb)
  * A non-trivial example of searching Jupyter Notebook code cells to find Python import statements.
  * Project: find which modules are imported most often in all Jupyter Notebooks found at or below the home directory.

### Seaborn / Matplotlib

- [Seaborn]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/Seaborn.ipynb)
  - Demonstrate several features of Seaborn plotting.

### Pandas
* [Pandas DataFrame Elements]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/Pandas01a.ipynb)
* [Data Selection]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/Pandas01b.ipynb)
  * **df[]** - 5 different ways to use it
  * **df.loc[]** - 10 different ways to use it
  * **df.iloc[]** - 8 different ways to use it
* [Additional Topics]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/Pandas01c.ipynb)
  * inplace vs return copy of modified value
  * index alignment
  * axis specification
* [IMDB Data Example]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/Pandas02.ipynb)
  * finding and using unique identifiers as DataFrame index
  * persist to hdf5 for further analysis in later notebook
  * 5 examples of simple queries
  * discussion on column types and Python data types
  * missing values and their implications on data type
* [Group By]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/Pandas03.ipynb)
  * Split, Apply, Combine
  * Equivalent of SQL Having Clause: Filter on Combined DataFrame
  * Plot using Seaborn
* [Tidy Data & Advanced Queries](http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/Pandas04.ipynb)
  * Tidy the Movie Data (both actors and genres are lists per cell before tidying)
  * Method Chaining to transform to tidy format
  * Aggregate with respect to genre and Query Examples
  * Aggregate with respect to actor and Query Examples
  * Advanced Query Examples

### Open Source Baseball Project

Analyze open source baseball data from Lahman and Retrosheet.  This project has moved to: https://github.com/sdiehl28/baseball-analytics

### Iterative Model Development with Scikit Learn

Iterative Model development is presented as a series of 10 notebooks.

For detail, see: [Iterative Model Development](/projects/iterative_model_dev/)

* [Model Development](https://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/TitanicN01.ipynb)
  * Definition of Scikit Learn Model
  * The Model Building Process
  * Ranking Models vs Evaluating Models
* [Visual Exploratory Data Analysis (EDA)](http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/TitanicN02.ipynb)
  * Understand Data Domain
  * Visually analyze *subset* of data to avoid Overfitting
* [Create First Model](http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/TitanicN03.ipynb)
  * Begin with most promising features found during EDA
  * Begin with simple or no preprocessing
  * Compare Model with Null Model
* [Cross Validation and Avoiding Data Leakage](http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/TitanicN04.ipynb)
  * What is Data Leakage
  * Feature Transformation with and without Data Leakage
* [Encapsulating Data Processing with Pipes](http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/TitanicN05.ipynb)
  * Use Numeric Features
  * Standardize and Impute missing values
  * Use v0.21 IterativeImputer
* [Encapsulating Data Processing with ColumnTransformer](http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/TitanicN06.ipynb)
  * Use v0.20 ColumnTransformer for Pipes per Feature
  * Use Extracted Numeric Features suggested by EDA
  * Encapsulate Feature Encoding and Feature Transformation in Functions
  * More on Data Leakage
* [Categorical Encoding](http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/TitanicN07.ipynb)
  * Use Extracted Categorical Features suggested by EDA
  * Encode Categorical Features
  * Refine Feature Encoding and Feature Transformation Functions
  * Simplify Model
* [Hyperparameter Optimization](http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/TitanicN08.ipynb)
  * One Standard Error Rule
  * Specialized Learning Curve for Best K for Model Ranking
  * Nested Cross Validation
* [Ensembles](http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/TitanicN09.ipynb)
  * Custom Code a Stacking Estimator
  * Tune Base Learners and Meta Learner
  * Use VotingClassifier
  * Custom Code a Forest of Decision Trees
* [Building an Interpretable Model](http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/TitanicN10.ipynb)
  * Build two small, simple, yet accurate Decision Trees
  * Use Decision Trees to explain the domain data
