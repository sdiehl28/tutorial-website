+++
title = "Jupyter Notebook TOC"
description = ""
weight = 10
alwaysopen = false
head = "<label>Jupyter Notebooks</label>"
lastmod = 2019-03-12

+++

### Python Programming
A basic understanding of Python and programming is assumed.  These notebooks illustrate some commonly misunderstood topics.

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

The most detailed open source baseball data available will be downloaded, unzipped, parsed, wrangled and persisted as both CSV files and Postgres tables.  For a full description of the project, see: TODO

* [Baseball 01]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/BB01-Intro.ipynb)
  * Download and unzip Lahman and Retrosheet baseball data.
* [Baseball 02]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/BB02-HelperFunctions.ipynb)
  * Define 10 functions used throughout the Baseball notebooks.
  * The most important being the ability to read/write to csv files while retaining DataFrame column types.
* [Baseball 03]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/BB03-DataOrganization.ipynb)
  * Overview of data organization and data dictionaries.  Hundreds of fields in total.
  * Data will be organized as multiple "tidy data" csv files and Postgres tables
* [Baseball 04]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/BB04-LahmanWranglePersist.ipynb)
  * Lahman: Wrangle and Persist to CSV and Postgres
* [Baseball 05]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/BB05-RetroParse.ipynb)
  * Retrosheet: parse play-by-play data to stats per player per game
  * Retrosheet: parse play-by-play data to stats per team per game
* [Baseball 06]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/BB06-RetroWranglePersistCSV.ipynb)
  * Retrosheet: wrangle data and persist to csv files
* [Baseball 07]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/BB07-RetroPersistPostgres.ipynb)
  * use df.to_sql() to create Postgres tables
  * bulk load large csv files into Postgres
* [Baseball 08]( http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/BB08-CompareRetroLahman.ipynb)
  * Compute several aggregates of the Retrosheet data and compare with Lahman data.

### Iterative ML Model Development -- Titantic DataSet

* [Create Baseline Model](http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/Titanic01.ipynb)
* [Cross Validation](http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/Titanic02.ipynb)
* [Custom Transformers](http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/Titanic03.ipynb)
* [Categorical Encoding](http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/Titanic04.ipynb)
* [Feature Extraction](http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/projects/titanic/Titanic05.ipynb)
