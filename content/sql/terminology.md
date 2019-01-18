---
title: Terminology
weight: 10
lastmod: 2019-01-18

# typora requires yaml, not toml
typora-root-url: /home/agni/WebSites/published/tutorial-website/static/
---

The following definitions are too short and simply to be fully accurate.  More detailed introductions can be found on Wikipedia and in textbooks.

#### Database

A database is a collection of data.

In practice, this term is often used to refer to not just the data, but to the software system which manages the data.  A more precise term for this usage is Database Management System (DBMS).

#### Database Management System (DBMS)

The software system which manages a database.

#### Relational Database Management System (RDBMS)

The software system which manages a database using the relational model.

#### Relational Model

A method of storing data in tables.  Columns in one table may reference columns in another table to form relations. 

A proper introduction would require many pages.  A data scientist may only need to understand Tidy Data rather than the full relational model.

#### Tidy Data

A term introduced by Hadley Wickham.  Loosely speaking, Tidy Data is the subset of the relational model that Data Scientists need to understand.  It is described using simpler terminology than than used in relational model.

Tidy data terms:

1. Variable: A quantity, quality, or property that you can measure.
2. Observation: A set of values that display the relationship between variables.  To be an observation, values need to be measured under similar conditions, usually measured at the same time.
3. Value: The state of the variable that you observe when you measure it.

Tidy data definition:

1. Each variable is in its own column
2. Each observation is in its own row
3. Each value is in its own cell

Relational data is tidy.  For most Data Scientists, it is sufficient to understand Tidy Data rather than the more formal relational model and its various normal forms.

#### NoSQL

NoSQL has no precise definition.  Most often it is used to mean any DBMS that does not store data in a relational model.

#### SQL

SQL is a language used to create, read, update and delete data.  It is almost always used for data stored in a relational model and it is seldom used for data not stored in a relational model.

SQL also includes statements for managing a RDBMS.

In practice, SQL is often used to refer to the software system which manages data using the relational model.  A more precise term for this usage is RDBMS.

The part of SQL that is used to create, read, update and delete data, is fundamentally based on relational algebra.