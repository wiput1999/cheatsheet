# UPDATE
```sql
UPDATE [table_name]
SET [column_name] = [value]
(WHERE condtion);
```

For example (**with** WHERE clause)
```sql
UPDATE sales_reps
SET salary = 10000
WHERE reps_id = 152;
```

Example (**without** WHERE clause)
```sql
UPDATE sales_reps
SET salary = 10000
```

## Set from same table

If you want to set a data to be in the same data as subqueries **but the data is in the same table**, user defined variable is required
```sql
SET @value_id := (
  SELECT address
  FROM loc
  WHERE loc_id = 1700
);
```

then you can update it using a variable
```sql
UPDATE loc
SET address = @value_id
WHERE loc_id = 2000;
```

This will result to loc_id number 2000
to have the same address as loc_id number 1700


## Set from different table

If you want to set a data to be in the same data as subqueries **but the data is in the different table**, you can start writing it after a `SET` queries.
```sql
UPDATE sales_reps
SET salary = (SELECT salary
              FROM employees
              WHERE employee_id = 115),

    commission_pct = (SELECT commission_pct
                      FROM employees
                      WHERE employee_id = 115)
WHERE reps_id = 151;
```
