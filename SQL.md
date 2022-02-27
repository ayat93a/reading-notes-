# Summary of Simple SELECT Queries
## A basic query code for selection , constraints Filtering and sorting
`SELECT column, another_column, …
FROM mytable
WHERE condition(s)
ORDER BY column ASC/DESC
LIMIT num_limit OFFSET num_offset;`
## To insert rows
`INSERT INTO mytable
VALUES (value_or_expr, another_value_or_expr, …),
       (value_or_expr_2, another_value_or_expr_2, …),
       …;`
## Updating rows
UPDATE mytable
`SET column = value_or_expr, 
    other_column = another_value_or_expr, 
    …
WHERE condition;`
## Deleting rows
`DELETE FROM mytable
WHERE condition;`
## Creating tables
`CREATE TABLE IF NOT EXISTS mytable (
    column DataType TableConstraint DEFAULT default_value,
    another_column DataType TableConstraint DEFAULT default_value,
    …
);`
## ALTER TABLE mytable
`ADD column DataType OptionalTableConstraint 
    DEFAULT default_value;`
## Dropping tables
`DROP TABLE IF EXISTS mytable;`

### Extra care should be Taken in deleting rows or drop table for the constraines
### THIS SAMPLES CODE IS FROM [SQLBOLT](https://sqlbolt.com/)



| LESSON        | Varification of complete it  |
|--------------|:-----:|
| 1 |[Exercise 1](./SQLBOLT/1.5.PNG)| 
| 2| [Exercise 2](/SQLBOLT/2.4.PNG)| 
| 3 |[Exercise 3](/SQLBOLT/3.4.PNG)| 
| 4 | [Exercise 4](./SQLBOLT/4.4.PNG)| 
| 5 |[Exercise 5](./SQLBOLT/5.5.PNG) | 
| 6 | [Exercise 6](./SQLBOLT/6.3.PNG)| 
| 13 |[Exercise 13](./SQLBOLT/13.2.PNG) | 
| 14 |[Exercise 14](./SQLBOLT/14.3.PNG) | 
| 15 | [Exercise 15](./SQLBOLT/15.2.PNG)| 
| 16 |[Exercise 16](./SQLBOLT/16.PNG) | 
| 17 | [Exercise 17](./SQLBOLT/17.2.PNG)| 
| 18 |[Exercise 18](./SQLBOLT/18.2.PNG) |

[Back](./README.md)
