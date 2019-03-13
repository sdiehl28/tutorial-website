+++
title = "Table of Contents"
description = ""
weight = 10
alwaysopen = false
head = "<label>Jupyter Notebooks</label>"
lastmod = 2019-03-13

+++

A list of Jupyter Notebooks I have created on github, organized by topic.

These notebooks are designed for use with Jupyter Lab and the Table of Contents extension: [JupyterLab TOC Extension](https://github.com/jupyterlab/jupyterlab-toc).

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
  * Python 3.6 NameTuple
  * Python 3.6 dataclasses
  * dict with value being list
  * iterator and iterable
  * closures

### Regular Expressions

A previous introduction to regular expressions would be helpful.

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

A previous introduction to matplotlib would be helpful.

- [Seaborn]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/Seaborn.ipynb)
  - Demonstrate several features of Seaborn plotting.

### Pandas
A basic understanding of numpy is assumed.

* [Pandas DataFrame Elements]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/Pandas01a.ipynb)
* [Data Selection]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/Pandas01a.ipynb)
  * **df[]** - 5 different ways to use it
  * **df.loc[]** - 10 different ways to use it
  * **df.iloc[]** - 8 different ways to use it
* [Additional Topics]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/Pandas01a.ipynb)
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

Analyze open source baseball data from Lahman and Retrosheet.

For detail see: [Baseball Data Analysis](/projects/baseball/)

* [Get Lahman & Retrosheet Data]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/BB01-Intro.ipynb)
* [Helper Functions]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/BB02-HelperFunctions.ipynb)
* [Data Organization & Data Dictionary]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/BB03-DataOrganization.ipynb)
* [Lahman: Wrangle and Persist]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/BB04-LahmanWranglePersist.ipynb)
* [Retrosheet: Parse Data]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/BB05-RetroParse.ipynb)
* [Retrosheet: Wrangle and Persist to csv]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/BB06-RetroWranglePersistCSV.ipynb)
* [Retrosheet: Persit to Postgres]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/BB07-RetroPersistPostgres.ipynb)
* [Lahman & Retrosheet: Aggregate and Compare]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/BB08-CompareRetroLahman.ipynb)

### Iterative ML Model Development

Iterative Model development is discussed using the Titantic data set from Kaggle for context.  

For detail, see: [Iterative Model Development](/projects/iterative_model_dev/)

* [Create Baseline Model](http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/Titanic01.ipynb)
* [Cross Validation](http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/Titanic02.ipynb)
* [Custom Transformers](http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/Titanic03.ipynb)
* [Categorical Encoding](http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/Titanic04.ipynb)
* [Feature Extraction](http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/Titanic05.ipynb)
