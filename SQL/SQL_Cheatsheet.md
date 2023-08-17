# SELECT Statement: Retrieving Data

SELECT column1, column2, ...
FROM table_name
WHERE condition
ORDER BY column_name
LIMIT n;

# INSERT Statement: Adding Data

INSERT INTO table_name (column1, column2, ...)
VALUES (value1, value2, ...);

# UPDATE Statement: Modifying Data

UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;

# DELETE Statement: Removing Data

DELETE FROM table_name
WHERE condition;

# Basic Filtering with WHERE

SELECT column1, column2, ...
FROM table_name
WHERE condition;

# Sorting with ORDER BY

SELECT column1, column2, ...
FROM table_name
ORDER BY column_name [ASC | DESC];

# Limiting Results with LIMIT

SELECT column1, column2, ...
FROM table_name
LIMIT n;

# Joining Tables

SELECT column1, column2, ...
FROM table1
JOIN table2 ON table1.column = table2.column;

# Grouping Data with GROUP BY

SELECT column1, COUNT(*)
FROM table_name
GROUP BY column1;

# Filtering Grouped Data with HAVING

SELECT column1, COUNT(*)
FROM table_name
GROUP BY column1
HAVING COUNT(*) > n;

# Combining Conditions with AND/OR

SELECT column1, column2, ...
FROM table_name
WHERE condition1 AND condition2;

# Wildcard Matching with LIKE

SELECT column1, column2, ...
FROM table_name
WHERE column_name LIKE pattern;

# Using Functions

SELECT function(column)
FROM table_name;

# Creating Tables

CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    ...
);

# Modifying Tables

ALTER TABLE table_name
ADD column_name datatype;

ALTER TABLE table_name
DROP COLUMN column_name;

ALTER TABLE table_name
MODIFY column_name datatype;

# Dropping Tables

DROP TABLE table_name;


# SQL Cheat Sheet

## Operators

| Operator | Description |
|---|---|
| `SELECT` | Retrieves data from a database |
| `INSERT INTO` | Inserts data into a database table |
| `UPDATE` | Updates data in a database table |
| `DELETE` | Deletes data from a database table |
| `WHERE` | Filters data based on a condition |
| `ORDER BY` | Sorts data in ascending or descending order |
| `GROUP BY` | Groups data together based on a common value |
| `HAVING` | Filters groups of data based on a condition |
| `JOIN` | Combines data from two or more tables |
| `UNION` | Combines the results of two or more SELECT statements |
| `INTERSECT` | Returns rows that are common to two or more SELECT statements |
| `EXCEPT` | Returns rows that are unique to one of two or more SELECT statements |

## Functions

| Function | Description |
|---|---|
| `COUNT()` | Counts the number of rows in a table |
| `SUM()` | Sums the values in a column |
| `AVG()` | Calculates the average value in a column |
| `MIN()` | Finds the minimum value in a column |
| `MAX()` | Finds the maximum value in a column |
| `CONCAT()` | Concatenates two or more strings |
| `SUBSTRING()` | Extracts a substring from a string |
| `LENGTH()` | Returns the length of a string |
| `UPPER()` | Converts a string to uppercase |
| `LOWER()` | Converts a string to lowercase |