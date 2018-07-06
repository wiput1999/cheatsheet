# WHERE
```sql
WHERE [argument]
```

WHERE keyword need to be used with `SELECT` argument

```sql
SELECT first_name FROM employee
WHERE first_name = 'Jeff';
```
## Where met certain criteria
```sql
WHERE first_name = 'Jeff';
```

## Using `and` / `or` / `not` with WHERE
```sql
SELECT first_name FROM employee
WHERE first_name = 'John'
AND last_name = 'Cena'
AND NOT id = 12;
```

## Using `LIKE` in WHERE
- `%` - represents zero, one, or multiple characters
- `_` - represents a single character

```sql
SELECT first_name FROM employee
WHERE first_name LIKE 'J%'
```

and it will results in the column that the first name **starts with ‘J’**

```sql
SELECT first_name FROM employee
WHERE first_name LIKE '%J'
```
and it will result in the column that the first name **ends with ‘J’**

```sql
SELECT first_name FROM employee
WHERE first_name LIKE 'J____'
```
and it will result in the column that the first name **starts with ‘J’ and have 4 more alphabet after it**

```sql
SELECT first_name FROM employee
WHERE first_name LIKE 'J_h_'
```
and it will result in the column that the first name **starts with ‘J’ and the third alphabet is ‘h’**

```sql
SELECT first_name FROM employee
WHERE first_name LIKE 'J%n'
```
and it will result in the column that the first name **starts with ‘J’ and ends with ‘n’**


## Using `IN` in WHERE
```sql
SELECT first_name FROM employee
WHERE first_name IN ('John', 'Jeff')
```
and it will result in the column that the first name **is either ‘John’ or ‘Jeff’**

```sql
SELECT first_name FROM employee
WHERE first_name NOT IN ('John', 'Jeff')
```
and it will result in the column that the first name **is neither ‘John’ nor ‘Jeff’**


## Using `BETWEEN` in WHERE
```sql
SELECT [column_name(s)] FROM [table_name]
WHERE [column_name] BETWEEN [value1] AND [value2];
```
Equivalent to `[value1] <= [column_name] <= [value2]` in Math equation

```sql
SELECT first_name FROM employee
WHERE salary BETWEEN 2000 AND 5000
```
and it will result in the column that the salary is between 2000 and 5000
