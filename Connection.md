# Connection

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
 

Ex: 
- [197. Rising Temperature](https://leetcode.cn/problems/rising-temperature/description/?envType=study-plan-v2&envId=sql-free-50)
---

References: 
- [MySQL LEFT JOIN](https://www.mysqltutorial.org/mysql-left-join.aspx)