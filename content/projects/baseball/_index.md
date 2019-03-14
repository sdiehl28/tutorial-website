+++
title = "Baseball"
description = ""
weight = 30
alwaysopen = false
lastmod = 2019-03-14

+++
The two most comprehensive open source data sets for Baseball are:

* Lahman
  * [Lahman Snapshot](http://www.seanlahman.com/baseball-archive/statistics)
  * [Lahman Most Recent](https://github.com/chadwickbureau/baseballdatabank)
* Retrosheet
  * [Retrosheet Play-by-Play](https://www.retrosheet.org/game.htm)

Both Lahman and Retrosheet will be downloaded, parsed, wrangled and persisted to both CSV files and Postgres in preparation for Analysis.  After which various types of analysis will be done.

It is not necessary to persist wrangled data to both CSV files and Postgres.  Doing both is for demonstration purposes, as both are common approaches.

[Sabermetrics ](https://en.wikipedia.org/wiki/Sabermetrics) is a bit like feature extraction for images.  Image recognition used to require complex processing such as "edge detection" to identify features that were then fed to machine learning algorithms.  With the advent of Deep Learning, this type of feature extraction is no longer necessary.

Sabermetrics are the "extracted features" from baseball data.  Usually they have to do with the value of a player with respect to winning a baseball game.  A few Sabermetrics about a player can convey a lot of information to a person familiar with these derived attributes.  Using them as input to a machine learning algorithm is likely to be helpful.  That said, this type of feature extraction is not absolutely necessary.

Sabermetrics, being a particular type of derived feature, will only be discussed briefly in what follows.  This is website is primarily about Data Science and Machine Learning.

If you are interested in Sabermetrics or Baseball in particular, you may enjoy the following: [Sabermetrics: How to Find Data](https://sabr.org/sabermetrics/data)
