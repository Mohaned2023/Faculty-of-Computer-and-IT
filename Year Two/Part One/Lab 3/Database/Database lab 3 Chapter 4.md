#### **Limiting the Rows Selected:**
- Restrict the rows returned by using the WHERE clause.
- The WHERE clause follows the FROM clause.
```sql
SELECT  *|{[DISTINCT] column|expression [alias],...}
FROM  table
[WHERE  condition(s)];
```

- ? Example:
```sql
SELECT 
	employee_id,
	last_name,
	job_id,
	department_id
FROM   employees
WHERE  department_id = 90 ;
```

#### **Character Strings and Dates:**
- Character strings and date values are enclosed in single quotation marks.
- Character values are case sensitive, and date values are format sensitive.
- The default date format is DD-MON-RR.

- ? Example:
```sql
SELECT  
	department_id,
	last_name,
	job_id
FROM   employees
WHERE  last_name = 'Whalen';
```


#### **Comparison Conditions:**

|           **Meaning**           |      **Operator**      |
| :-----------------------------: | :--------------------: |
|            Equal to             |           =            |
|          Greater than           |           >            |
|    Greater than or equal to     |           >=           |
|            Less than            |           <            |
|      Less than or equal to      |           <=           |
|          Not equal to           |           <>           |
| Between two values (inclusive), | BETWEEN  <br>...AND... |
|  Match any of a list of values  |        IN(set)         |
|    Match a character pattern    |          LIKE          |
|         Is a null value         |        IS NULL         |
- ? Example:
```sql
SELECT 
	last_name, 
	salary
FROM   employees
WHERE  salary <= 3000;
```

- ? Example:
```sql
-- BETWEEN
SELECT 
	last_name,
	salary
FROM   employees
WHERE  salary BETWEEN 2500 AND 3500;

-- IN()
SELECT 
	employee_id, 
	last_name, 
	salary, 
	manager_id
FROM   employees
WHERE  manager_id IN (100, 101, 201);

-- LIKE with %
SELECT  
	first_name
FROM   employees
WHERE  first_name LIKE 'S%';

-- LIKE with _ _
SELECT 
	last_name
FROM   employees
WHERE  last_name LIKE '_o%';

-- IS
SELECT 
	last_name,
	manager_id
FROM   employees
WHERE  manager_id IS NULL;
```

#### **Logical Conditions:**

| Meaning                                            | Operator |
| -------------------------------------------------- | :------: |
| Returns TRUE if both component conditions are true |   AND    |
| Returns TRUE if either component condition is true |    OR    |
| Returns TRUE if the following  condition is false  |   NOT    |
- ? Example:
```sql
-- AND
SELECT 
	employee_id,
	last_name,
	job_id,
	salary
FROM   employees
WHERE  salary >= 10000
AND    job_id LIKE '%MAN%';

-- OR
SELECT 
	employee_id, 
	last_name, 
	job_id, 
	salary
FROM   employees
WHERE  salary >= 10000
OR     job_id LIKE '%MAN%';

-- NOT
SELECT 
	last_name,
	job_id
FROM   employees
WHERE  job_id
NOT IN ('IT_PROG', 'ST_CLERK', 'SA_REP');
```


#### **Rules of Precedence:**

| Order Evaluated | Operator                    |
| :-------------: | :-------------------------- |
|        1        | Arithmetic operators        |
|        2        | Concatenation operator      |
|        3        | Comparison conditions       |
|        4        | IS NOT  NULL, LIKE,  NOT IN |
|        5        | NOT BETWEEN                 |
|        6        | NOT logical condition       |
|        7        | AND logical condition       |
|        8        | OR logical condition        |
- ? Example:
```sql
SELECT 
	last_name,
	job_id,
	salary
FROM   employees
WHERE  job_id = 'SA_REP'
OR     job_id = 'AD_PRES'
AND    salary > 15000;

SELECT 
	last_name,
	job_id,
	salary
FROM   employees
WHERE  (job_id = 'SA_REP' OR job_id = 'AD_PRES')
AND    salary > 15000;
```


#### **ORDER BY Clause:**
- Sort rows with the ORDER BY clause
	- **ASC:** ascending order, default
	- **DESC:** descending order
- The ORDER BY clause comes last in the SELECT statement.
- ? Example:
```sql
-- ASC
SELECT   
	last_name,
	job_id,
	department_id,
	hire_date
FROM     employees
ORDER BY hire_date ;

-- DSEC
SELECT   
	last_name, 
	job_id, 
	department_id,
	hire_date
FROM     employees
ORDER BY hire_date DESC ;

-- Sorting by Column Alias
SELECT 
	employee_id,
	last_name, 
	salary*12 annsal
FROM   employees
ORDER BY annsal;

-- Sorting by Multiple Columns
SELECT 
	last_name,
	department_id,
	salary
FROM   employees
ORDER BY department_id, salary DESC;
```