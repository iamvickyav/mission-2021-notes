# SQL

## MySQL DB

MySQL -> Server -> Instance -> Running

To interact with MySQL Server -> Use Workbench/Studio

MySQL URL in local - http://localhost:3306

- RDBMS --> Table -> Rows & Columns (imagine Excel)

- Intersection of Row & Column -> Cell

- Cell holds the value

- Table -> Stored in Storage ->

- CRUD Operations -> Create, Read, Update, Delete ??

- SQL -> Structured Query Language -> SQL Queries used to perform CRUD Operations

## Create a Database

```sql
create database itech_db;

show databases;

use itech_db;
```

## Create a table

```sql
CREATE TABLE employee (
    id INT,
	name VARCHAR(20),
	designation VARCHAR(20),
	dept VARCHAR(10),
	PRIMARY KEY (id)
);
```

## Read from table

```sql
SELECT * FROM employee

SELECT * FROM employee WHERE id =1
```

## Insert into table

```sql
INSERT INTO employee (id, name, designation, dept)
    values (2, 'Vandhana', 'CTO', 'Management');
INSERT INTO employee (id, name, designation, dept)
    values (3, 'Lakshman', 'BOSS', 'Management');
INSERT INTO employee (id, name, designation, dept)
    values (4, 'Ajitha', 'Developer', 'Team');
INSERT INTO employee (id, name, designation, dept)
    values (5, 'Rohinth', 'Senior Developer', 'Team');
```

## Update in table

```sql
UPDATE employee SET designation = 'Senior Developer' WHERE id=4;
```

## Delete in table

```sql
DELETE FROM employee WHERE id=6;
```

## Count from table

```sql
SELECT COUNT(id) FROM employee WHERE dept = 'Management';

SELECT COUNT(id) AS EMP_COUNT FROM employee WHERE dept = 'Management';
```

## Like Queries

```sql
SELECT * FROM employee WHERE name LIKE '%an';

SELECT * FROM employee WHERE name LIKE '%a%';

SELECT * FROM employee WHERE name LIKE 'a%';

SELECT * FROM employee WHERE name LIKE '_i%';
```
