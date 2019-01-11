+++
title = "Nested Cross Validation"
description = ""
weight = 30
draft = false
lastmod = 2018-05-09
typora-root-url = "/home/agni/SoftwareProjects/Sites/tutorial/static/"
+++
[Cross Validated](https://stats.stackexchange.com/), an excellent source for information about machine learning, statistics and related subjects, has several questions regarding Nested Cross Validation.  These questions include:

* what is it?
* when should it be used?
* what does it accomplish? do I get hyperparameter values?
* what should I do after (nested) cross validation?

Cross Validated has some excellent responses, especially those by [Cawley](https://stats.stackexchange.com/questions/64991/model-selection-and-cross-validation-the-right-way#72324) who goes by the alias Dikran Marsupial on the site.  Cawley has also coauthored excellent papers such as: [On Over-fitting in Model Selection and Subsequent Selection Bias in Performance Evaluation](http://jmlr.org/papers/v11/cawley10a.html)

There are also many excellent resources on Cross Validation.  Here are a few excellent videos:

* [Selecting the best model in scikit-learn using cross-validation](https://www.youtube.com/watch?v=6dbrR-WymjI)
* [ISL 1](https://www.youtube.com/watch?v=_2ij6eaaSl0&list=PL5-da3qGB5IA6E6ZNXu7dp89_uv8yocmf)
* [ISL 2](https://www.youtube.com/watch?v=nZAM5OXrktY&list=PL5-da3qGB5IA6E6ZNXu7dp89_uv8yocmf)
* [ISL 3](https://www.youtube.com/watch?v=S06JpVoNaA0&list=PL5-da3qGB5IA6E6ZNXu7dp89_uv8yocmf)

The purpose of the following 3 Jupyter Notebooks is not to teach the concepts so much as it is to demonstrate them with working code.  The concepts are well described in words by others, but given that there are still many questions, it seems the concepts could be made more concrete with actual code examples.  That is what is done here.

I believe there are 2 primary reasons for not understanding new material:

* the presentation does not resonate with the student
* the student doesn't fully grasp the prerequisite material

#### Presentation Should Resonate

When trying to learn something new, it is very important to take the time to find presenters who explain things in a way that resonates with how you think.  Too many students simply go with the first hit or two on Google and then wonder why those resources were not helpful.  You are better off briefly reviewing a dozen or more resources to see which one is most appropriate for you, and then spending time with those specific resources.

#### Prerequisite Material

Too often a student who is stuck on a "hard" topic proceeds to bang their head against the wall trying to figure it out, but nothing seems to help.  If you find yourself in that situation, then the solution is often to review the prerequisite material and come back to the "hard" material later.  With the right preparation, the hard material will no longer seem hard.

#### Nested Cross Validation

I believe Nested Cross Validation is not inherently difficult.  I believe the issue for most people is that Scikit Learn methods do so much work behind the scenes that the full scope of what is happening is not fully understood.  If the methods were understood in detail, then understanding how to put them together, and how they relate to key machine learning concepts, is not difficult.

As such, I have created 3 Jupyter notebooks which go over in detail what the Scikit Learn methods are doing behind the scenes.  For many, this may seem like too much review, and yet if you go through them in order, the final notebook on Nested Cross Validation will be easy to understand.

#### Jupyter Notebooks

1. Cross Validation using a Pipeline with cross_val_score()
2. GridSearchCV
3. Nested Cross Validation

### Summary
