---
title: Working with Databases
weight: 20
lastmod: 2020-01-03

# typora requires yaml, not toml
typora-root-url: ../../../static
---

### SQL vs NoSQL

"SQL vs NoSQL" is usually used to mean, "Relational vs Non-Relational modeling of data".

For an excellent discussion on how best to decide between SQL and NoSQL, see: [NoSQL Distilled: Emerging Polyglot Persistence by Martin Fowler and Parmod J. Sadalage](https://www.amazon.com/NoSQL-Distilled-Emerging-Polyglot-Persistence/dp/0321826620/).

Several use cases were discovered in the early 2000s for which the relational model is not optimal.

Here are a few examples:

- documents, such as web pages or log files (use MongoDB or similar)
- network connections, such as Facebook connections (use Neo4j or similar)
- high performance key-value lookups, such as an amazon shopping cart (use Redis or similar)

Based on my personal experience in the industry, many people between about 2005 and 2015 believed that the RDBMS was going to be almost entirely replaced with a "NoSQL" solution.  However over the last few years, the power of the relational model, built upon the fundamental mathematics of relational algebra, has been reaffirmed and most people in the industry today feel that the RDBMS is not going away any time soon.

### Working with Data in an RDBMS

For data analysis, it is often useful to pull the data from the RDBMS into memory (or into an abstraction that allows the application to treat the data as if it were in memory).

In R, Hadley Wickham's Tidyverse set of packages borrow heavily from the syntax of SQL, and allows for relational operations to be performed on R Dataframes.  Hadley Wickham references E. F. Codd and relational algebra in his discussion of his design of his Tidyverse packages.

In Python, Pandas allows for relational operations.  The Pandas syntax and terminology is less closely tied to SQL than it is with the Tidyverse packages, but a significant subset of Pandas is devoted to relational operations on Pandas DataFrames.

Other options include:

- using the Python's Standard Library's DB-API specification to work almost directly with SQL.  For example, using [psycopg2](http://initd.org/psycopg/) to interact with PostgreSQL.
- using SQL Alchemy's Core API, which is a lightweight abstraction over SQL.
- using SQL Alchemy's ORM API, which is a Object-Relational-Mapper that generates SQL.

It is often said that there is an "impedance mismatch" between the relational model and the object model used in object oriented programming (OOP).  For an object oriented programmer, an Object Relational Mapper (ORM) can be a helpful tool.  That said, in my experience, at least one person on a development team must be an expert with RDBMS otherwise the use of an ORM (or even a SQL API) can be misused resulting in poor performance.

### Relational Database Management Systems

Per [DB Engines](https://db-engines.com/en/ranking_trend) in December 2019, PostgreSQL is the fastest growing Database Management System and the fourth most popular overall.  It remains well behind the big three; Oracle MySQL and Microsoft SQL Server, however these three are in gradual decline.

#### Some Observations

The top four Database Management Systems are all Relational.  The fifth is MongoDB which is document oriented.

The top three relational open source systems are MySQL, PostgreSQL, and SQLite.  For an excellent comparison see: [SQLite vs MySQL vs PostgreSQL](<https://www.digitalocean.com/community/tutorials/sqlite-vs-mysql-vs-postgresql-a-comparison-of-relational-database-management-systems>)

Since 2014, PostgreSQL has doubled in popularity, whereas the top three RDBMS products have all declined slightly.

For learning SQL (and the basics of RDMBS administration), I would recommend PostgreSQL.  It has many features that are missing from SQLite and MySQL.  An excellent book on learning SQL with PostgreSQL is: [Practical SQL by Anthony DeBarros](<https://www.amazon.com/Practical-SQL-Beginners-Guide-Storytelling-ebook/dp/B07197G78H/>).

For deploying an application, the best open source RDMBS depends on your application needs.  See the above link comparing SQLite, MySQL and PostgreSQL.