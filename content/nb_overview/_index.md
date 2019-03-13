+++
title = "Jupyter Notebooks"
description = ""
weight = 30
alwaysopen = false
lastmod = 2019-01-19

+++

### Jupyter Notebooks and IDEs

The easiest way to learn and experiment is to use Jupyter Notebooks.

A Jupyter notebook is like a scientist's lab book.  It provides the ability to:

* enter HTML formatted notes using simple markdown, next to each mini code experiment
* execute a block of code and get immediate text or graphical feedback
* serve as a reminder as to what has been learned

The easiest way to be efficient in a professional programming environment is to use an IDE.  An IDE offers:

* context aware highlighted editing
* style checking to ensure other developers can easily read your code
* easy access to online library help
* ability to set breakpoints, examine variable values, and step through code
* and much more

The choice of an IDE is a personal matter.  The following IDEs (with their appropriate plug-ins), are excellent:

* [PyCharm](https://www.jetbrains.com/pycharm/download/)
* [Atom](https://atom.io/)
* [Sublime](https://www.sublimetext.com/)

It is important to note that a Jupyter Notebook serves a different purpose than an IDE.  A Jupyter Notebook is good for exploration, whether it's experimenting with corner cases of an API, or it's Exploratory Data Analysis.   And IDE allows for efficient software development in which the code is intended to be maintained over a period of time by multiple developers.

A free service which makes it easy to share Jupyter notebooks with others is [nbviewer](https://nbviewer.jupyter.org/).  Nbviewer also offers the option to download the Jupyter Notebook it is displaying or execute it on Binder.

All the links on this website use nbviewer to display my Jupyter Notebooks.  Simply click on the link.  For example: [Show Versions](https://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/snippets/ShowVersions.ipynb)

To use Binder from the nbviewer page, simply click on the 3 ring icon in the top right of the nbviewer page.  This will take you to the binder site where you will be allowed to execute the Jupyter Notebook and make temporary changes to it.  For details about how Binder works see: [MyBinder How It Works](https://mybinder.org/#how-it-works)

### Using Jupyter Lab for Jupyter Notebooks

Complex notebooks are easier to maintain using Jupyter Lab which provides tabs for each notebook, and the ability cut and paste between notebooks.  It also has add-ons such as [Table of Contents](https://github.com/jupyterlab/jupyterlab-toc
) which is automatically derived from header levels in the notebook.  The notebooks here are designed to be easier to follow by using the Table of Contents add-on.  Note that add-ons for Jupyter Lab are different than add-ons for Jupyter Notebook.

### Operating System

Most of the Jupyter Notebooks on this site will run identically under Linux or MacOS or Windows.  All notebooks were tested on Ubuntu 18.04 LTS running Anaconda Distribution 2018.12 or later.

### Python Package Versions

The package versions I am using on my workstation, as of March, 2019, can be seen with: [Show Versions](
http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/snippets/ShowVersions.ipynb)

I am using the Anaconda distribution which I highly recommend for learning purposes.  See [Getting Started](/getting_started)

If you install a recent version of Anaconda, your packages will be the same or later and these notebooks should work the same in your environment.

