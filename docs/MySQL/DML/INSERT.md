# INSERT INTO
INSERT INTO [table name]
VALUES ([value1], [value2] ...);

For example
```sql
INSERT INTO lab_location(location_id,location_name)
VALUES (002,'Rayong'),(003,'Ranong');
```

or you can skip the table column, when you want to fill all column
```sql
INSERT INTO lab_location
VALUES (002,'Rayong'),(003,'Ranong');
```

but the **values need to have the same value size + data type as the table**


## Insert with `NULL` value

WARNING : Adding NULL value to the table may result in column / table conflicts

For example
```sql
INSERT INTO lab_location(location_id)
VALUES (002);
```
Avoid to add a `location_name` will results it to become `NULL` value.

```sql
INSERT INTO lab_location
VaLUES (002, NULL)
```
Saying that the `location_name` will be `NULL`
