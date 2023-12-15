# Connection
## MySQL `(INNER) JOIN`
The `INNER JOIN` clause compares each row in `t1` table with every rown in the `t2` table in a one-to-one fashion, based on the joining condition.

```MySQL
SELECT * FROM t1
JOIN t2 ON join_condition;
```

The order of t1 and t2 does not matter. 

### Combining with `GROUP BY`
It is common to use `GROUP BY` with `JOIN`: 

```MySQL
SELECT column1, column2, FUNCTION(column3) as new_column FROM t1
JOIN t2 ON join_condition
GROUP BY column1, column2
ORDER BY new_column;
```
`JOIN` is just combining information side by side; it doesn't provide useful information, until we use `GROUP BY` and any aggregation functions to do analysis.

## MySQL `LEFT JOIN`

### Using `LEFT JOIN` clause to join two tables:

`LEFT JOIN` allows us to query data from two or more tables.

```MYSQL
SELECT 
    select_list
FROM
    t1
LEFT JOIN t2 ON 
    join_condition;
```

Ex: 
- [1378. Replace Employee ID With The Unique Identifier](https://leetcode.cn/problems/replace-employee-id-with-the-unique-identifier/description/?envType=study-plan-v2&envId=sql-free-50)
- [1068. Product Sales Analysis I](https://leetcode.cn/problems/product-sales-analysis-i/description/?envType=study-plan-v2&envId=sql-free-50)


### Using `LEFT JOIN` clause to find unmatched rows:

If there is no matching from the left table `t1` to the right table `t2`, columns from the right row will contain `NULL`. `LEFT JOIN` will still return all rows from the left regardless if there is a matching or not. In this case, we can find non mathcing rows (`is NULL`).

Ex:
- [1581. Customer Who Visited but Did Not Make Any Transactions](https://leetcode.cn/problems/customer-who-visited-but-did-not-make-any-transactions/description/?envType=study-plan-v2&envId=sql-free-50)


## MySQL `CROSS JOIN`
 the `CROSS JOIN` clause returns a Cartesian product of rows from the joined tables.
```MySQL
SELECT select_list 
FROM t1
CROSS JOIN t2;
```
### MySQL `TIMESTAMPDIFF()` Function

The `TIMESTAMPDIFF()` function returns the difference between two datetime expressions in years, months, days, hours, minutes, or seconds.
```MySQL
TIMESTAMPDIFF(unit, begin, end);
```
The TIMESTAMPDIFF function returns the result of `begin` - `end`, where `begin` and `end` are `DATE` or `DATETIME` expressions.

The unit argument determines the unit of the result of (`end - begin`) represented as an integer. The following are valid units:
`MICROSECOND`, `SECOND`, `MINUTE`, `HOUR`, `DAY`, `WEEK`, `MONTH`, `QUARTER`, `YEAR`.

Ex: 
- [197. Rising Temperature](https://leetcode.cn/problems/rising-temperature/description/?envType=study-plan-v2&envId=sql-free-50)



---



References: 
- [MySQL LEFT JOIN tutorial](https://www.mysqltutorial.org/mysql-left-join.aspx)
- [MySQL CROSS JOIN tutorial](https://www.mysqltutorial.org/mysql-cross-join/)
- [MySQL TIMESTAMPDIFF() Function tutorial](https://www.mysqltutorial.org/mysql-timestampdiff/)