# SQL ressources


## Functions (MySQL, Postgres, BigQuery)

```SUBSTRING(_string_, _start_, _length_)```    Character offset starts at 1

```CAST(field_name AS newtype)```    Dealing with different datatypes

```LEN(string)```    Length of a string

```CONCAT('SQL', ' is', ' fun!')```     Two or more strings

```CONTAINS (column_name, 'search_pattern')```


## More Commands

```DISTINCT``` Remove duplicates


## Filtering

```<>``` not equal to

```BETWEEN``` between these two values


## Aggregate

```SUM()```  Returns the total of all values.

```AVG()```  Returns the mean average of all values.

```COUNT()```  Counts and returns the number of values.

```MIN()```  Returns the smallest value.

```MAX()```  Returns the largest value.


## INNER JOIN

Returns only Matching Records

```SELECT table.field FROM first_table INNER JOIN second_table ON first_table.field = second_table.field;```

INNER is the default join type for JOIN (you can just write JOIN)






