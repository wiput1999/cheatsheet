# INNER JOIN

## Join with `ON` clause
```sql
SELECT *
FROM table1
JOIN table2
  ON (tablee1.column_name = table2.column_name)
```

## Creating Three-way joins with ON clause
```sql
SELECT employee_id, city, department_name
FROM employees e
JOIN departments d
  ON (e.department_id = d.department_id)
  JOIN locations l
ON (d.location_id = l.location_id)
```

## Specified table using ON clause
```sql
SELECT [attribute1]
FROM employees e
JOIN employees m
ON (e.id = m.id)
```

To join other attribute in same table (recursive relationship)
