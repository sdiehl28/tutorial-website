---
title: "Pandas Access Specification"
description: ""
weight: 50
alwaysopen: true
lastmod: 2018-05-03
typora-root-url: /home/agni/SoftwareProjects/Sites/tutorial/static/
---

If you are coming to Python from another language, then the "axis specification" may seem backwards as used in Numpy and Pandas.  That is, specifying the axis to be "rows" seems to act like a column specification and vice versa.  

Also, the Pandas API is arguably inconsistent when it comes to axis specification, with one set of rules applying to mathematical like operations (being consistent with numpy) and another set of rules applying to data modifying operations.  Being inconsistent and being different from most other languages, makes it frustrating at first.  Here is my Jupyter Notebook on the topic: <a href="http://nbviewer.jupyter.org/github/sdiehl28/tutorial-jupyter-notebooks/blob/master/sklearn/AxisSpecification.ipynb" target="_blank">Pandas Axis Specification
</a>