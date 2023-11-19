# Query
## MySQL IS NULL

`IS NULL`/ `IS NOT NULL`

MySQL does not have a built-in BOOLEAN type. It uses `TINYINT(1)` to represent the BOOLEAN values: TRUE means 1 and FALSE means 0.
`IS NULL` is a comparison operator for anything that is UNKNOWN, including NULL itself.

Syntax: 
```
value IS NULL
```

Example: [Leetcode 584. Find Customer Referee](https://leetcode.cn/problems/find-customer-referee/?envType=study-plan-v2&envId=sql-free-50)

In this example, we'll take extra care for the comparisons as it contains `NULL`


## MySQL ORDER BY
To sort the rows in the result set, add `ORDER BY` clause in the  `SELECT` statement.

Syntax:
```
SELECT 
   select_list
FROM 
   table_name
ORDER BY 
   column1 [ASC|DESC], 
   column2 [ASC|DESC],
   ...;
```

`ASC` stands for ascending. `ORDER BY` will sort the values in the `column1` in the ascending order: 
```
ORDER BY column1 ASC
```

`DESC` stands for descending, similarly.
```
ORDER BY column2 DESC
```

If you don't specify any option, `ORDER BY ` will sort the value ascendingly:
``` 
ORDER BY column1
```

Example: [Leetcode 1148. Article Views I](https://leetcode.cn/problems/article-views-i/description/?envType=study-plan-v2&envId=sql-free-50)

---

## References:
- https://www.mysqltutorial.org/mysql-order-by/
- https://www.mysqltutorial.org/mysql-where/