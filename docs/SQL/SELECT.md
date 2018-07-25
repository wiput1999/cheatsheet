# SELECT
```sql
SELECT [column_name] FROM [table_name]
```

## Select all from table
```sql
SELECT * FROM employee
```

## Select some column from table
```sql
SELECT first_name, last_name FROM employee
```

## Select `DISTINCT` column
```sql
SELECT DISTINCT salary FROM employee
```

the result will not have duplicates (because using `DISTINCT` keyword)

## Modify the result with calculations
```sql
SELECT salary, salary * 100 FROM employee
```

and that will show the salary column and the column that is a value of the salary times 100.

## Temporary change column name with `AS`
```sql
SELECT first_name AS `First Name` FROM employee
```

`AS` keyword also can be skipped.
NOTE : use backslash \` to marked it as a string


## Use `CONCAT` to merge row-column value
```sql
SELECT concat(last_name, ' is a ', job_id) AS `Employee Details` FROM employee
```
