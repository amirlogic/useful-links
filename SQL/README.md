# SQL ressources

## Exercises

https://www.sql-practice.com

https://learnsql.com


## Functions (MySQL, Postgres, BigQuery)

```SUBSTRING(_string_, _start_, _length_)```    Character offset starts at 1

```CAST(field_name AS newtype)```    Dealing with different datatypes

```LEN(string)```    Length of a string

```CONCAT('SQL', ' is', ' fun!')```     Two or more strings

```CONTAINS (column_name, 'search_pattern')```


## More Commands

```DISTINCT``` Removes duplicates

```EXISTS (subquery)``` Returns TRUE if the subquery returns at least one row, otherwise it returns FALSE


## Filtering

```<>``` not equal to

```BETWEEN``` between these two values

```IS NULL``` and ```IS NOT NULL```


## Aggregate

```SUM()```  Returns the total of all values.

```AVG()```  Returns the mean average of all values.

```COUNT()```  Counts and returns the number of values.

```MIN()```  Returns the smallest value.

```MAX()```  Returns the largest value.

```GROUP BY``` in combination with ```HAVING```


## INNER JOIN

Returns only Matching Records

```sql
SELECT table.field FROM first_table INNER JOIN second_table ON first_table.field = second_table.field;
```

INNER is the default join type for JOIN (you can just write JOIN)


## Pattern search

```WHERE column LIKE pattern```

Percentage (% ) wildcard matches a sequence of any character including space

Underscore ( _ ) wildcard matches any single character


## Window Functions



## Date

Default format is YYYY-MM-DD

```YEAR``` Extracts year from a date


## Remember

When using nested queries, the query inside parentheses runs first, and then its result is used in the outside query

