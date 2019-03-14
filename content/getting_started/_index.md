+++
title = "Getting Started"
description = ""
weight = 110
alwaysopen = false
head = "<label>Recommendations</label>"
lastmod = 2019-03-14

+++

### Python vs R

Here I am expressing my personal opinions as a software developer with a mathematics background.  Someone else, with a different background, may have different opinions.

Data Science and Machine Learning concepts can be easier to learn in R.  Hadley Wickham's packages modernize R and are superbly designed and written.  Hadley's packages are cleaner and clearer than their Pandas counterparts.  Unfortunately this is only true for exploratory data analysis, in which the data analyst sits down and works with data in a single R session.  As soon as this work needs to be converted to production code that must be maintained by others, R loses its advantage.

Python is a well proven software development language.  Developers on a Python software development team will likely have had experience with such [DevOps ](https://en.wikipedia.org/wiki/DevOps) practices as unit testing, continuous integration, Docker, etc.  Whereas a R user is often not part of a software developer team and rarely has exposure to [DevOps ](https://en.wikipedia.org/wiki/DevOps) (or [DataOps](https://en.wikipedia.org/wiki/DataOps)) which is essential for deploying real-world solutions.

Sometimes students complain that their course is given in R, when they intend to work in the "real world" with Python.  I would argue that nothing is lost learning Data Science and Machine Learning in R.  The concepts, as long as Hadley's tidyverse set of packages is used, are easier to understand in R.  However once the concepts are understood, Python is the better language for business software development.

Another objection that is often raised is that it takes too much time to learn both R and Python.  I would agree.  A younger person just getting started would likely benefit by spending the time to learn both.  A busy professional may prefer to focus on Python.

This website will use Python for most discussions and examples.

### What is a "Beginner"?

The term "beginner" is a relative term.  To someone with 10 years of experience, a "beginning" topic might be something that anyone with 3 years of experience should know.  Whereas to someone with 1 year of experience, a "beginning" topic might be something that anyone with 3 months of experience should know.

It can be frustrating to come across "beginning" material that is incomprehensible.  What this actually means is that the material is not really beginning material, or that it is not well presented.

I firmly believe that there is no such thing as a "hard topic".  Rather there are topics for which one is not prepared, and trying to learn a topic without the proper preparation is not only hard, but viritually impossible.

If you find that something is not making sense, then there are two things to do.  First, try to find the same material from a different presenter.  You need to feel comfortable with both the presenter and the presentation.  In university settings, sometimes a professor is someone who has a research grant and they have little or no interest in teaching but are required to teach.  It is hard to learn from such "teachers".  Instead the material must be learned elsewhere.

If after searching for alternative presentations, the material still does not makes sense, this does not mean the material is too hard for you, rather it means you would probably benefit from a review of the prerequisite material.  I find that frustration with learning is almost always associated with a "rushed" mindset.  If I am in a hurry, I skip over as many prerequisites as possible, but then get tripped up trying to understand the topic I actually care about.  I find it is necessary to slow down and review the prerequisite material, and then approach the "hard" topic.

Online courses are very helpful.  I would recommend taking as many as you have time for.  That said, real-world proficiency is only going to come about through working on a project in which you are forced to work with, in actual code, the techniques you have learned.

### Development Environment

All code here uses the Anaconda distribution of Python.   There are many excellent Anaconda installation tutorials on the web, such as:
<a href="https://www.youtube.com/watch?v=YJC6ldI3hWk" target="_blank">Installing Anaconda</a>

### JupyterLab

As of the time of this writing, [JupyterLab](https://jupyterlab.readthedocs.io/en/stable/) is in beta, but it is ready for use.  JupyterLab is a great way to develop Jupyter notebooks.  I would also recommend the JupyterLab extensions for spell checking and table-of-contents.