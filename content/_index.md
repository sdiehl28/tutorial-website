+++
title = "Home Page"
description = "Home Page"
creatordisplayname = "Stephen Diehl"
lastmodifierdisplayname = " by Stephen Diehl"
lastmod = 2018-02-28
+++

### Software Nirvana
**2018-02-28: Under Construction: Website and Jupyter Notebooks not yet written!**

A website about Python, Data Science, Machine Learning and related topics.

#### Preface

This website was motivated by observing that the majority of "Kaggle Kernels" published to help novice machine learners, make the very serious mistake of "data leakage".  This is true even of kernels published by some of Kaggle's own staff.

Perhaps the thinking is that it's too hard to teach beginners a correct machine learning workflow, so let's present an easier, albeit seriously flawed workflow instead.  I disagree with this approach.  Unlearning a bad habit can be more difficult than learning a new good habit.

If you do not know what "data leakage" is, that's fine.  It will be defined shortly.  For now it is important to realize that "data leakage" may lead to improperly tuned models as well as highly inflated estimates of model accuracy on out-of-sample data.  These are serious problems in the real world usage of predictive models.  "Data leakage" is a part of the larger topic of "overfitting"and more generally this website will focus on avoiding overfitting.

As the Kaggle tutorials that most often exhibit data leakage refer to the Kaggle Titanic dataset, this is the dataset that will be used here.  But this website won't be yet another rehash of predicting on the Titanic dataset, rather it will be a clear step-by-step presentation of the entire machine learning workflow, with an emphasis on code, that allows the beginner to apply what they learn here to more complex real world problems.

The approach presented here will borrow from the ideas of agile software development.  The idea is that continuous measured improvement through iteration leads to a better solution than trying to approach software development in a linear (aka waterfall) fashion.

Machine Learning involves many steps and the steps are interconnected with one another.  It is not possible to simply follow a predefined set of steps, in order, and arrive at the "best" model on the last step.    Rather a more organic approach in which a baseline model is quickly created, a metric of success is measured and documented, and the model is improved through a series of iterations in which any step of the model building process may be modified, will be used.

Machine Learning is a vast topic that relies on many disciplines.  The intent of this website is not to teach machine learning, but rather to teach a *process* for creating a machine learning model that borrows from success stories in software development.  That said, to get hung up on process, the names used for process steps, etc., is to miss the forest from the trees.  What matters is the organic evolution of your machine learning model through a series of iterative cycles each of which measure improvement.  What name you give it and and exactly how you do it, is irrelevant.  The only thing that is relevant is success.

#### Who This is For

Beginning and intermediate practitioners of Data Science and Machine Learning.

It is assumed you have written some Python, Pandas and Scikit Learn code, but may not be comfortable putting all the pieces together.

#### Projects

The best way to learn is to work on an actual project.  The first project will orient around the Kaggle introductory competition for the Titantic dataset.  Within the context of refining the predictive modeling workflow for the Titantic competition, short tutorials will be presented.

#### Tutorials

For each topic, a short introduction will be presented with links to Jupyter Notebooks.  The Jupyter Notebooks will be the primary teaching tool.  Code will be emphasized over theory, but the code will be carefully explained.

#### Posts and Reviews of Books, Courses and Tools

Data Science and Machine Learning are built on top of many disciplines, each of which has a large number of topics in their own right.  As such, Data Science and Machine Learning encompasses a vast number of topics.  Beginners are often overwhelmed at the number of books and courses recommended, *just to get started*.  But no one can *start* with dozens of resources at once.  And yet it is necessary to get started somewhere.

My goal here will be to provide just the most important (in my opinion) resources in order to make "getting out the door" possible.

> It's a dangerous business, Frodo, going out your door.  You step onto the road, and if you don't keep your feet, there's no knowing where you might be swept off to.

J.R.R. Tolkien, The Lord of the Rings












