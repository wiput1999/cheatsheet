# CREATE TABLE
```sql
CREATE TABLE table_name (
column1 datatype,
column2 datatype,
column3 datatype,
   ....
);
```

## Create new employee table
```sql
CREATE TABLE employee2 (
employee2_id INT(10),
first_name   VARCHAR(255),
last_nameVARCHAR(255),
salary   INT(10)
);
```

## Adding `PRIMARY KEY` constraints
```sql
CREATE TABLE employee2 (
employee2_id INT(10),
first_name   VARCHAR(255),
last_nameVARCHAR(255),
salary   INT(10),
PRIMARY KEY 'PK_first_name' (first_name)
);
```

## Adding `FOREIGN KEY` constraints
```sql
CREATE TABLE employee2 (
employee2_id INT(10),
first_name   VARCHAR(255),
last_nameVARCHAR(255),
salary   INT(10),

FOREIGN KEY (employee2_id) REFERENCES employee(employee_id)
);
```

This bounds the `employee2_id` as a foreign key to the table `employee` with column `employee_id`.

but adding optional items to the rule is simple

1. `ON DELETE CASCADE` will delete dependent row when mother table is deleted
2. `ON DELETE SET NULL` will set foreign key that cannot be referenced as NULL

by adding these constraints, the row will delete safely (able to delete normally). If not, the reference integrity will blocked you from deleting the row.

## Adding `NOT NULL` constraints
```sql
CREATE TABLE employee2 (
employee2_id INT(10),
first_name   VARCHAR(255) NOT NULL,
last_nameVARCHAR(255) NOT NULL,
salary   INT(10)  NOT NULL,
);
```

## Adding `UNIQUE` constraints
```sql
CREATE TABLE employee2 (
employee2_id INT(10),
first_name   VARCHAR(255),
last_nameVARCHAR(255),
salary   INT(10),

UNIQUE (first_name, last_name)
);
```

## Create table from sub-queries
```sql
CREATE TABLE employee2
AS
SELECT first_name, last_name, salary FROM employee
WHERE salary BETWEEN 2000 AND 5000
```

As the SQL, it will runs

1. Starts query subquery
```sql
SELECT first_name, last_name, salary FROM employee
WHERE salary BETWEEN 2000 AND 5000
```

then

2. Then use the result to create a new table
```sql
CREATE TABLE employee2 AS ...
```
