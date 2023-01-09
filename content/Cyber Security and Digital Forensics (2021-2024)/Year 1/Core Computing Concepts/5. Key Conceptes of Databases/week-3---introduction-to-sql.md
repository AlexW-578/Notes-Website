---
title: Week 3 - Introduction to SQL
description: ""
date: 2023-01-08T22:30:25.996Z
preview: ""
draft: false
tags: ""
categories: ""
lastmod: 2023-01-08T23:23:11.641Z
---
# Introduction to SQL
## What is SQL?
- Structured Query Language (SQL)
- Developed by IBM (system R) in the 1970's
- SQL is used to communicate with a database
- Based on the relational model
- E/R Designs can be implemented in SQL
- Provides a DDL, DML, and a DCL

- DDL - Data Definition Language (Create, Alter, Drop)
	- CREATE DATABASE
	- ALTER DATABASE
	- CREATE TABLE
	- ALTER TABLE
	- DROP TABLE
	- CREATE INDEX
	- DROP INDEX
- DML - Data Manipulation Language (Select, Update, Delete, Insert)
	- SELECT
	- UPDATE
	- DELETE
	- INSERT INTO
- DCL - Data Control Language (Grant, Revoke)
	- GRANT
	- REVOKE

## SQL Language Elements
- SQL keywords are NOT case sensitive
	- **Select** is the same as **SELECT**
	- SQL keywords are normally written in uppercase for emphasis
![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220604145151.png)

## SQL Data Types
- Numeric
	- bit
	- tinyint
	- smallint
	- bigint
	- decimal
	- numeric
	- float
	- real
- Date/Time
	- Date
	- Time
	- Datetime
	- Timestamp
	- Year
- Character/String
	- Char
	- Varchar
	- Varchar (max)
	- NText
- Unicode Character/String
	- NChar
	- NVarchar
	- NVarchar (max)
	- NText
- Binary
	- Binary
	- Varbinary
	- Varbinary (max)
	- Image
- Miscellaneous
	- Clob
	- Blob
	- XML
	- JSON

## ERD to SQL
![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220604145918.png)
- Departments -> A table called Departments
	- Columns for dID, dName, and dBudget

### Creating a Table in SQL
To create a table you need to provide:
- A name for the table
- A list of column definitions
- A List of constraints (such as keys)

```
CREATE TABLE "tablename" (
"column1" "DATATYPE" [CONSTRAINT], 
"column2" "DATATYPE" [CONSTRAINT], 
"column3" "DATATYPE" [CONSTRAINT]
);
```


#### Column Definitions
- Each column has a name and a type
	- *e.g.* INT, DATE, CHAR(n)
- Columns can be specified as NULL or NOT NULL
- Columns can be given a default value
	- Just use the keyword DEFAULT followed by the value
		- *e.g.* num INT DEFAULT 0

```sql
CREATE TABLE employee (
first VARCHAR(15) NOT NULL,
last VARCHAR(20) NOT NULL,
age NUMBER(3),
address VARCHAR(30),
city VARCHAR(20),
county VARCHAR(20)
);
```


#### SQL Constraints
- Constraints are the rules enforced on the **data columns of a table**
- Used to limit what type of data is entered into the table
- Constraints could be either on a **column level** or a **table level**
	- The **column level** constraints are applied **only to one column**
	- The **table level** constraints are applied to the **whole table**

##### PRIMARY KEY Constraint
- Primary key constraints uniquely identifies each record in a database
- Can not accept NULL

```sql
CREATE TABLE Student(
stuID INT PRIMARY KEY,
Name VARCHAR(60),
Age INT
)
```

##### FOREIGN KEY Constraint
- Foreign key is used to generate the relationship between the tables
- Foreign key is a field in the database table that is Primary key in another table
- This is sometimes also called as a referencing key
- Can accept NULL

```sql
CREATE TABLE Enrolment (
enrCode CHAR(6) PRIMARY KEY,
enrAssignment INT,
enrExam INT, 
stuID INT FOREIGN KEY REFERENCES Student(stuID)
);
```

##### NOT NULL Constraint
- Ensures that a column cannot have NULL value since by default a column can hold NULL values

```sql
CREATE TABLE Student(
stuID INT NOT NULL,
Name VARCHAR(60),
Age INT
);
```

##### DEFUALT Constraint
- Provides a default value for a column when none is specified
	- *e.g.*
	- if INSERT INTO statement does not provide a specific value
```sql
CREATE TABLE Student(
stuID INT NOT NULL,
Name VARCHAR(60),
Age INT DEFAULT 0
);
```

##### UNIQUE Constraint
- Ensures that all values in a column are different
- This constraint can be applied at the column level or table level

```sql
CREATE TABLE Student(
stuID INT NOT NULL UNIQUE,
Name VARCHAR(60),
Age INT
);
```

##### CHECK Constraint
- Ensures that all the values in a column satisfies certain conditions
```sql
CREATE TABLE Student(
stuID INT NOT NULL CHECK(stuID > 0),
Name VARCHAR(60),
Age INT
);
```


### Deleting Tables
- Use DROP TABLE statement to **remove a table definition** and all the data, indexes, triggers,  constraints, and permissions specifications for that table
 ```sql 
 DROP TABLE table_name;
 ```
- **Note** - You should be very careful while using this command as it **executes immediately** with **no confirmation**. This could result in **permanent data loss**.

### ALTER TABLE
- ALTER TABLE command is used to **add**, **delete** or **modify columns** in an existing table
- You can also use the ALTER TABLE command to **add** and **drop** various **constraints** one a table

#### Add a New Column:
```sql
ALTER TABLE table_name ADD COLUMN column_name DATATYPE;
```
*e.g.*
```sql
ALTER TABLE Student ADD COLUMN Degree VARCHAR(50);
```

#### Drop Column:
```sql
ALTER TABLE table_name DROP COLUMN column_name;
```
*e.g.*
```sql
ALTER TABLE Student DROP COLUMN Degree;
```

#### Change the DATA TYPE:
```sql
ALTER TABLE table_name MODIFY COLUMN column_name DATATYPE;
```
*e.g.*
```sql
ALTER TABLE Student MODIFY COLUMN Year INT;
```

#### ADD Constraint
```sql
ALTER TABLE table_name ADD CONSTRAINT MyUniqueConstraint;
```
*e.g.*
```sql
ALTER TABLE employee_details ADD CONSTRAINT pk_emp_name PRIMARY KEY (emp_name);
```

#### DROP Constraint
```sql
ALTER TABLE table_name DROP CONSTRAINT MyUniqueConstraint;
```
*e.g.*
```sql
ALTER TABLE employee_details DROP CONSTRAINT pk_emp_name;
```

#### INSERT INTO
- Used to add new rows of data to a table in the database
- There are two basic syntaxes of the INSERT INTO statement
1. Add values to specific columns using names
```sql
INSERT INTO table_name (column1, column2, column3, ...columnN) VALUES (value1, value2, value3, ...columnN);
```
2. Adds values to specific columns using placement
```sql
INSERT INTO table_name VALUES (value1, value2, value3, ...valueN);
```

![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220604164326.png)

#### SELECT
- Used to query a database and retrieve selected data that math the criteria that was specified
- Can be used to select one column, a comma-separated list of columns, and \* for all columns
```sql
SELECT column1, column2, columnN FROM table_name;

SELECT * FROM table_name;
```
*e.g.*
```sql
SELECT stuFName, stuAddress FROM Student;
```
*Put Notes Here*





## Videos:

