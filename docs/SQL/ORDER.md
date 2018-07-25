# ORDER BY
```sql
SELECT [column1], [column2], ...
FROM [table_name]
ORDER BY [column1], [column2], ... [ASC|DESC];
```

ORDER BY keyword **sorts the records in ascending order by default**.
To sort the records in descending order, use the DESC keyword.

For example
```sql
SELECT first_name, last_name, salary
FROM employee
ORDER BY first_name, last_name DESC
```
This will sort the `first_name` first. If the first_name is duplicated, `last_name` will be used to sort those conflict off.
