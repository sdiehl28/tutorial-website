---
title: Data Terms
weight: 10
lastmod: 2019-01-18

# typora requires yaml, not toml
typora-root-url: /home/agni/WebSites/published/tutorial-website/static/
---

The following definitions are too short and simple to be fully accurate.  More detailed introductions can be found on Wikipedia and in textbooks.

#### Database

A database is a collection of data.

In practice, this term is often also used to refer to the software system which manages the data.  A more precise term for this usage is Database Management System (DBMS).

#### Database Management System (DBMS)

The software system which manages a database.

#### Relational Database Management System (RDBMS)

The software system which manages a relational database. This is the most common type of database system in use today.

#### Relational Model

A method of storing data in tables with observations represented as rows and variables represented as columns.  Columns in one table may reference columns in another table to form relations. 

A proper introduction would require many pages.  A data scientist may only need to understand "Tidy Data"  (see below) rather than the full relational model.

#### Tidy Data

A definition created by Hadley Wickham.  Loosely speaking, Tidy Data refers to the subset of the relational model that is needed by data scientists.  In relational terminology, Tidy Data is very similar to a table in third normal form.

"Tidy Data" refers to the structure of the data.  Tidy data can be used equally well in both R and Python.  

In R, data (optionally structured as tidy data), is handled with the set of packages called the [Tidyverse](https://www.tidyverse.org/packages/).  In Python, data (optionally structured as tidy data), is handled primarily with [Pandas](https://pandas.pydata.org/).

In the following, I am using a some of Hadley's words from his [tidy data paper](https://vita.had.co.nz/papers/tidy-data.pdf) and some of my own words to make it clearer.

Tidy data terms:

1. Variable: A quantity, quality, attribute or property that you can measure.  For example a person's weight is a variable.  It is called a variable because it's values can vary.
2. Value: The state of the variable when you measure it.  For example, 180 pounds.
3. Observation: A set of values measured for all attributes of a given unit (such as person) often measured at the same time.  For example, person_id = 123-456-7890, weight=180 pounds, heart rate = 78 bpm, at 3 pm on January 1st, 2019.
4. Table: the type of observational unit.  For example, a table of measurements of people.

Tidy data definition:

1. Each variable is in its own column
2. Each observation is in its own row
3. Each value is in its own cell
4. Each type of observational unit in its own table (or dataframe)

#### NoSQL

NoSQL has no precise definition.  Most often it is used to mean any DBMS that does not store data in a relational model.

#### SQL

SQL is a language used to create, read, update and delete data.  It is almost always used for data stored in a relational model and it is seldom used for data not stored in a relational model.

SQL also includes statements for managing a RDBMS.

In practice, SQL is often also used to refer to the software system which manages relational data.  A more precise term for this usage is RDBMS.