#### **Basic SELECT Statement:**
- SELECT identifies what columns
- FROM identifies which table

```sql
SELECT  *|{[DISTINCT] column|expression [alias],...}
FROM  table;
```

- Selecting All Columns:

```sql
SELECT *
FROM   departments;
```

- Selecting Specific Columns:

```sql
SELECT department_id, location_id
FROM   departments;
```

#### **Writing SQL Statements:**
- SQL statements are not case sensitive.
- SQL statements can be on one or more lines.
- Keywords cannot be abbreviated or split across lines.
- Clauses are usually placed on separate lines.
- Indents are used to enhance readability.

#### **Arithmetic Expressions:**
Create expressions with number and date data by using arithmetic operators.

| Operator | Description |
| -------- | ----------- |
| +        | Add         |
| -        | Subtract    |
| *        | Multiply    |
| /        | Divide      |
- Example:

```sql
SELECT 
	last_name,
	salary,
	salary + 300
FROM   employees;

-- Operator Precedence
SELECT 
	last_name,
	salary, 
	12*salary+100
FROM   employees;

-- Using Parentheses
SELECT 
	last_name,
	salary,
	12*(salary+100)
FROM   employees;
```

#### **Defining a Null Value:**
- A null is a value that is unavailable, unassigned, unknown, or inapplicable.
- A null is not the same as zero or a blank space.

- Example:

```sql 
SELECT 
	last_name,
	job_id,
	salary,
	commission_pct -- Null Column
FROM   employees;

-- Null Values in Arithmetic Expressions
SELECT 
	last_name,
	12*salary*commission_pct
FROM   employees;
```

#### **Defining a Column Alias:**
- Renames a column heading
- Is useful with calculations
- Immediately follows the column name - there can also be the optional AS keyword between the column name and alias
- Requires double quotation marks if it contains spaces or special characters or is case sensitive

- Example:

```sql
SELECT 
	last_name AS name, -- Rename with as
	commission_pct comm -- without as
FROM   employees;

-- Spaces 
SELECT 
	last_name "Name", 
	salary*12 "Annual Salary" -- The name has space.
FROM   employees;
```

#### **Concatenation Operator:**
- Concatenates columns or character strings to other columns
- Is represented by two vertical bars ( || )
- Creates a resultant column that is a character expression

- Example:

```sql
SELECT  
	last_name || job_id AS "Employees"
FROM   employees;

-- Using Literal Character Strings
SELECT 
	last_name  ||' is a '|| job_id AS "Employee Details"
FROM   employees;
```

#### **Duplicate Rows:**
- The default display of queries is all rows, including duplicate rows.

```sql
SELECT department_id
FROM   employees;

-- Eliminating Duplicate Rows
SELECT DISTINCT department_id
FROM   employees;
```



