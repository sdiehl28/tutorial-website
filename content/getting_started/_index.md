+++
title = "Getting Started"
description = ""
weight = 110
alwaysopen = false
head = "<label>Recommendations</label>"
lastmod = 2020-02-05

+++

### Python vs R

As of February 2020, it is clear that Python is winning the Data Science battle with R.

![image-20200205101505542](/home/agni/WebSites/published/tutorial-website/static/images/tiobe-2020-02-05-R.png)

![image-20200205101619523](/home/agni/WebSites/published/tutorial-website/static/images/tiobe-2020-02-05-Python.png)

Focusing on the period from 2015 to present, R had an excellent run-up from 2015 through 2018, but has declined the last 2 years, whereas Python has increased dramatically over the last 2 years.

In what follows, I am expressing my personal opinions as a software developer with a mathematics background.  Someone else, with a different background, may have different opinions.

Data Science and Machine Learning concepts can be easier to learn in R.  Hadley Wickham's packages modernize R and are superbly designed and written.  Hadley's packages are cleaner and clearer than their Pandas counterparts.  Unfortunately this is only true for exploratory data analysis, in which the data analyst sits down and works with data in a single R session.  As soon as this work needs to be converted to production code that must be maintained by others, R loses its advantage.

Python is a well proven software development language.  Developers on a Python software development team will likely have had experience with such [DevOps ](https://en.wikipedia.org/wiki/DevOps) practices as unit testing, continuous integration, Docker, etc.  Whereas a R user is often not part of a software developer team and rarely has exposure to DevOps which is essential for deploying real-world solutions.

Sometimes students complain that their course is given in R, when they intend to work in the "real world" with Python.  I would argue that nothing is lost learning Data Science and Machine Learning in R.  The essential concepts, as long as Hadley's tidyverse set of packages is used, are easier to understand in R.  However once the concepts are understood, Python is the better language for business software development.

Another objection that is often raised is that it takes too much time to learn both R and Python.  I would agree.  A younger person just getting started would likely benefit by spending the time to learn both.  A busy professional may prefer to focus on Python.

This website will use Python for most discussions and examples.

### What is a "Beginner"?

The term "beginner" is a relative term.  To someone with 10 years of experience, a "beginning" topic might be something that anyone with 3 years of experience should know.  Whereas to someone with 1 year of experience, a "beginning" topic might be something that anyone with 3 months of experience should know.

It can be frustrating to come across "beginning" material that is incomprehensible.  What this means is that either the presentation is not right for your mindset, or you are not prepared for that level of material.

If you find that something is not making sense, then there are two things to do.  First, try to find the same material from a different presenter.  You need to feel comfortable with both the presenter and the presentation.  In university settings, sometimes a professor is someone who has a research grant and they have little or no interest in teaching but are required to teach.  It is hard to learn from such "teachers".  Instead the material must be learned elsewhere.

If after searching for alternative presentations, the material still does not makes sense, this does not mean the material is too hard for you, rather it means you would probably benefit from a review of the prerequisite material.  I find that frustration with learning is almost always associated with a "rushed" mindset.  If I am in a hurry, I skip over as many prerequisites as possible, but then get tripped up trying to understand the topic I actually care about.  I find it is necessary to slow down and review the prerequisite material, and then approach the "hard" topic.

Online courses can be very helpful.  I highly recommend taking several to get started.  That said, real-world proficiency is only going to come about through working on a project in which you are forced to work with the techniques you have learned by writing code.

### Development Environment

All code here uses the [Anaconda distribution](https://www.anaconda.com/distribution/) of Python.

In a production environment, it is important to create the minimal environment necessary in order to minimize application maintenance.  As such, the [Miniconda](<https://docs.conda.io/en/latest/miniconda.html>) distribution (also from Anaconda) may be more appropriate or a custom Python virtual environment created with pip.

### JupyterLab and Jupyter Notebook

JupyterLab and Jupyter Notebook are great ways to experiment and learn.

JupyterLab may run slow with a large notebook (even after the release of JupyterLab 1.0).  As such, it may be preferable to use Juypter Notebook until the performance of JupterLab is as good as that of Jupyter Notebook.