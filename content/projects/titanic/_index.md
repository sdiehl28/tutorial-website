---
title: "Iterative Model Development"
description: ""
weight: 10
alwaysopen: false
lastmod: 2018-04-27
---
Building a predictive model is an iterative process.  The goal is to quickly get something working and then evolve the model as seems best after analysis of the previous model.

At the highest level, the Model Development Process is:

- create a baseline model
- iteratively improve upon that model

*The model building process will be demonstrated using a series of Jupyter Notebooks with each notebook representing the next evolution of the model.*

Each web page will describe an overview of the topic and will link to a Jupyter Notebook representing one iteration of the model.

The iterative model development cycle consists of:

* setup (data wrangling)
* execution and results (measuring model performance)
* analysis (what worked, what didn't and what to try next)

For each iteration, the goal is to improve the model.  Improvement means:

- improve accuracy or interpretability
- improve software workflow

The benefits of improved software workflow include:

- reproducibility
- experimental flexibility
- reduced software and model evaluation bugs

#### Next

For the first iteration, we will create a simple model and measure its accuracy with cross validation.
