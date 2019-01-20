---
title: Working with Databases
weight: 20
lastmod: 2019-01-18

# typora requires yaml, not toml
typora-root-url: /home/agni/WebSites/published/tutorial-website/static/
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

A data scientist who interacts with an RDBMS, will likely encounter one of the top four most popular systems.

Per [DB Engines](https://db-engines.com/en/ranking_trend) in January 2019, the trends for the four most popular RDBMS:

![DB Rankings Image](/images/DB-Rankings-2019-01-18.png)

PostgreSQL is rapidly increasing in use while the top three are gradually declining in use.  This is in part because the top three have very high licensing fees and PostgreSQL is free, open-source, and with over 30 years of development, reliable and full featured.