# SQL
 
  
## Overview
SQL, or Structured Query Language, is a language designed to allow both technical and non-technical users to query, manipulte, and transform data from a relational database. Because of it's simplicity, SQL databases provide safe and calable storage for millions of websites and mobile applications.

## SQLBOT Notes
To retrieve data from a SQL database, we need to write SELECT statements, or queries. A query in itself is just a statement which declares what data we are looking for, where to find it in the database, and,  optionally, how to transform it before it is returned. It has a specific syntax.

SELECT column, another_column, ...
FROM mytable;<br>

The result of the above query will be a copy of the table but only with the columns that were requested. To retrieve all of the columns, use an *.

SELECT *
FROM mytable;<br>

This will display the whole table. Also, a comma can be used to select multiple columns. 
In order to filter certain results from being returned, we need to use a WHERE clause in the query. The clause is applied to each row of data by checking specific column values to determine whether it should be included in the results or not. Example:

SELECT column, another_column, ...
FROM mytable
WHERE condition
    AND/OR another_condition
    AND/OR ...;

More complex clauses can be constructed by joining numerous AND or OR logical keywords (ie. num_wheels >= 4 AND doors <= 2). And below are some useful operators that you can use for numerical data (ie. integer or floating point):


| Operator  | Condition | SQL Example
| ---------------- | ---------------- | ---------------- |
| =, !=, <, <=, >, >=| Standard Numerical operators |col_name != 4 |
| BETWEEN … AND …  | 	Number is within range of two values (inclusive) |	col_name BETWEEN 1.5 AND 10.5 |
|NOT BETWEEN … AND … | Number is not within range of two values (inclusive) | col_name NOT BETWEEN 1 AND 10|
| IN (…) | Number exists in a list | col_name IN (2, 4, 6) |
| NOT IN (…)| Number does not exist in a list | col_name NOT IN (1, 3, 5) |

### Reading Links
[SQL BOLT](https://sqlbolt.com/) <br>
[Practice SQL](https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_all) <br>

[Return to Homepage](https://claudiobailon.github.io/reading-notes/301.html)


 
>Education is not the learning of facts,
>but the training of the mind to think.
> -- <cite>[Albert Einstein][1]</cite>

[1]:https://www.goodreads.com/quotes/6137386-education-is-not-the-learning-of-facts-but-the-training 