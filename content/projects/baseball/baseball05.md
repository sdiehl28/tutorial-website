+++
title = "Parse Retrosheet Data"
description = ""
weight = 70
alwaysopen = false
lastmod = 2019-03-14
typora-root-url = "/home/agni/SoftwareProjects/Sites/tutorial/static/"

+++

#### Notebook: [Parse Retrosheet Data](http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/python/BB05-RetroParse.ipynb)

#### Goals
* Download Source Code for Open Source Parsers, build and install them OR use prebuilt Windows Binaries for these parsers.
* Run two parsers on the Retrosheet play-by-play data:
  * cwdaily parser: produces player per game stats
  * cwgame parser: produces team per game stats
* Each of the two parsers created a csv file per year.  Collect these yearly files into two DataFrames.

#### Next

Wrangle and Persist to CSV files.
