+++
title = "Virtual Environments"
date = 2019-01-14T21:49:18-08:00
lastmod = 2019-01-15
weight = 10
draft = false

+++

### Purpose
The purpose of having a virtual environment is to ensure that the set of packages you use are consistent with one another.  Whenever a package is updated, it may break another package that relies upon it.  Keeping track of a set of consistent packages, that is also as recent as possible, is very time consuming and error prone.

#### Anaconda Virtual Environment
Anaconda, which I recommend for learning Data Science and Machine Learning, automatically ensures that the packages you download into your virtual environment are consistent with one another.  When you upgrade a package, you will see "Solving Environment" for several tens of seconds.  What is happening is that Anaconda is determining, among all the packages installed in your virtual environment via Anaconda's package manager conda, which packages it can download that will work properly together.

#### Python Virtual Environment
Python also has the ability to create a virtual environment similar to Anaconda's virtual environment.  The difference is you, the developer, are responsible deciding which versions of which packages you want to have installed.  If you are a Python package developer, this is the level of control you want to have. If you are a user of Python packages, and particularly if you are learning rather than writing production code, you probably will be better off with conda's virtual environment rather than Python's.

One exception to this is if you want to install and run a Python based application.  Particularly if that Python application is packaged as a wheel.  A wheel is a set of packages determined to work well for a particular application.  In this case, you should create a Python virtual environment and pip install the wheel into that environment.  You generally would not install any other Python packages into that particular environment.

An example of a Python package that is best installed in a Python virtual environment is pgadmin4.  This is a Python flask application that interfaces with PostgreSQL.  To run pgadmin4, you should activate the Python virtual environment for pgadmin4, and then kick of pgadmin4.

#### When to use pip Instead of conda

Pip, which provides access to [Pypi](https://pypi.org/) works well inside a conda virtual environment.  Be sure to active your conda virtual environment before using pip to install anything.  The primary downside of using pip is that conda's "solving environment" will not know if the pip installed package is consistent with the packages installed with conda.   For this reason, its best to use conda for all packages directly available from the default Anaconda channel.  A "channel" is a repository of Anaconda packages.

That said, some packages are not commonly used for data science and are out of date or completely missing from Anaconda's default channel.  Although there are other channels (repos) available besides the default one, I prefer to use pip if I am not happy with what is available in the default Anaconda channel.  My reasoning is that the main Anaconda channel has a lot of testing done with it, and Pypi also has well tested packages.  I am less certain about other sources of Python packages.






