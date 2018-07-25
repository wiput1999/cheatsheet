# ALTER - ADD----------------------------------
## Add more rows to the table
ALTER TABLE table_name
ADD column_name datatype;


## Adding constraints to the table
ALTER TABLE lab_location
ADD PRIMARY KEY (location_id);

this will set `location_id` to be primary key


## Adding `Foreign Key` to the table
ALTER TABLE lab_location
ADD CONSTRAINT 'lab_emp_fk'
FOREIGN KEY (location_id)
REFERENCES lab_location(location_id);


## Adding `UNIQUE` to the table
ALTER TABLE lab_location
ADD UNIQUE (location_id)

or

ALTER TABLE lab_location
ADD CONSTRAINT 'UNIQUE_location_id' UNIQUE (location_id);

# ALTER - MODIFY----------------------------------
## Edit column data type
ALTER TABLE table_name
MODIFY COLUMN column_name datatype;

For example

ALTER TABLE employees
MODIFY last_name VARCHAR(25) NULL;

all of the column name, data type is also required to change the constraints `NULL`


## Change `NULL` to `NOT NULL` to the table
ALTER TABLE lab_location
MODIFY location_id VARCHAR(255) NOT NULL;

# ALTER - DROP----------------------------------
## Delete column
ALTER TABLE table_name
DROP COLUMN column_name;


## Delete `Primary Key / Foreign Key` constraints
ALTER TABLE lab_location
DROP PRIMARY KEY;

or

ALTER TABLE lab_location
DROP FOREIGN KEY 'lam_emp_fk';

## Delete `UNIQUE` constraints

Unique constraints cannot be removed without the name of the constraints.

ALTER TABLE lab_loction
DROP INDEX loc_name_un;
