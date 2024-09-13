#### Functions:
- **Single-row functions:**
	- Manipulate data items
	- ! Accept arguments and return one value
	- Act on each row returned
	- ! Return one result per row
	- May modify the data type
	- Can be nested
	- Accept arguments which can be a column or an expression
- Multiple-row functions.
#### Single-row functions:
- @ **Character functions:**
	- @ Case-manipulation functions:
		1. LOWER
		2. UPPER
		3. INITCAP
	- @ Character-manipulation functions:
		1. CONCAT
		2. SUBSTR
		3. LENGTH
		4. INSTR
		5. LPAD | RPAD
		6. TRIM
		7. REPLACE
- @ Number functions:
	1. ROUND
	2. TRUNC
	3. MOD
- @ Date functions:
	- SYSDATE
	- MONTHS_BETWEEN
	- ADD_MONTHS
	- NEXT_DAY
	- LAST_DAY
	- ROUND
	- TRUNC

#### Case-manipulation functions:
- How to use:
```sql
LOWER('SQL Course')   -- sql course
UPPER('SQL Course')   -- SQL COURSE
INITCAP('SQL Course') -- Sql Course
```
- Example: 
```sql
SELECT employee_id, last_name, department_id
FROM employees
WHERE LOWER(last_name) = 'higgins';
```

#### Character-Manipulation Functions:
- How to use:
```sql
CONCAT('Hello', 'World')    -- HelloWorld
SUBSTR('HelloWorld',1,5)    -- Hello
LENGTH('HelloWorld')        -- 10
INSTR('HelloWorld', 'W')    -- 6
LPAD(salary,10,'*')         -- *****24000
RPAD(salary, 10, '*')       -- 24000*****
TRIM('H' FROM 'HelloWorld') -- elloWorld
```
- Example:
```sql
SELECT 
	employee_id, 
	CONCAT(first_name, last_name) NAME,
	job_id,
	LENGTH(last_name),
	INSTR(last_name, 'a') "Contains 'a'?"
FROM employees
WHERE SUBSTR(job_id, 4) = 'REP';
```

#### Number Functions:
- How To use:
```sql
ROUND(45.926, 2) -- 45.93
TRUNC(45.926, 2) -- 45.92
MOD(1600, 300)   -- 100
```
- Example:
```sql
-- ROUND
SELECT 
	ROUND(45.923,2),
	ROUND(45.923,0),
	ROUND(45.923,-1)
FROM DUAL;

-- TRUNC
SELECT 
	TRUNC(45.923,2),
	TRUNC(45.923),
	TRUNC(45.923,-2)
FROM DUAL;

-- MOD
SELECT 
	last_name,
	salary,
	MOD(salary, 5000)
FROM employees
WHERE job_id = 'SA_REP';
```

#### Working with Dates:
- Oracle database stores dates in an internal numeric format: century, year, month, day, hours, minutes, seconds.
- The default date display format is `DD-MON-RR`.
	- Allows you to store 21st century dates in the 20th century by specifying only the last two digits of the year.
	- Allows you to store 20th century dates in the 21st century in the same way.
- Example:
```sql
SELECT 
	last_name, 
	hire_date -- Return a Date from the database.
FROM employees
WHERE last_name LIKE 'G%';

-- SYSDATE
SELECT 
	last_name, 
	(SYSDATE-hire_date)/7 AS WEEKS
FROM employees
WHERE department_id = 90;
```
- Date Functions:
```sql
MONTHS_BETWEEN('01-SEP-95','11-JAN-94') -- 19.6774194
ADD_MONTHS('11-JAN-94',6)               -- '11-JUL-94'
NEXT_DAY('01-SEP-95','FRIDAY')          -- '08-SEP-95'
LAST_DAY('01-FEB-95')                   -- '28-FEB-95'
ROUND('25-JUL-95','MONTH')              -- '01-AUG-95'
ROUND('25-JUL-95','YEAR')               -- '01-JAN-96'
TRUNC('25-JUL-95','MONTH')              -- '01-JUL-95'
TRUNC('25-JUL-95','YEAR')               -- '01-JAN-95'
```
