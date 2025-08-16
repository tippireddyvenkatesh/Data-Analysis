\# Week 3 – Advanced SQL



\## ✅ Topics Covered



\### 1. Joins

\- \*\*INNER JOIN\*\* → Returns rows with matching values in both tables.

\- \*\*LEFT JOIN\*\* → Returns all rows from the left table + matched rows from the right.

\- \*\*RIGHT JOIN\*\* → Returns all rows from the right table + matched rows from the left.

\- \*\*FULL OUTER JOIN\*\* → Returns all rows when there is a match in either table.

\- \*\*SELF JOIN\*\* → A table joins with itself.



📌 Joins let us combine data from multiple tables — essential for relational databases.



---



\### 2. UNION vs UNION ALL

\- \*\*UNION\*\* → Combines results of two queries and removes duplicates.

\- \*\*UNION ALL\*\* → Combines results of two queries and keeps duplicates.



📌 Useful when merging data sets from multiple sources.



---



\### 3. Subqueries

\- \*\*Scalar Subquery\*\* → Returns a single value.

\- \*\*IN with Subquery\*\* → Checks if a value exists in a subquery result.

\- \*\*Correlated Subquery\*\* → Refers to columns in the outer query (runs row by row).



📌 Subqueries allow building complex conditions and filtering using dynamic results.



---



\### 4. Window Functions (Analytic Functions)

\- \*\*ROW\_NUMBER()\*\* → Assigns unique sequential numbers to rows.

\- \*\*RANK()\*\* → Ranks rows, but gaps exist if ties happen.

\- \*\*DENSE\_RANK()\*\* → Similar to RANK but no gaps.

\- \*\*NTILE(n)\*\* → Divides rows into n groups (quartiles, percentiles, etc.).

\- \*\*LEAD() / LAG()\*\* → Access next/previous row’s value without self-joins.



📌 Advanced analytics — trend analysis, ranking, moving averages.



---



\### 5. String Functions

\- \*\*UPPER()\*\* → Converts text to uppercase.

\- \*\*LOWER()\*\* → Converts text to lowercase.

\- \*\*SUBSTR()\*\* → Extracts substring from text.

\- \*\*TRIM()\*\* → Removes spaces.

\- \*\*CONCAT()\*\* → Combines strings.



📌 Vital for data cleaning, formatting, and text-based analysis.



---



\### 6. Date Functions

\- \*\*SYSDATE / CURRENT\_DATE\*\* → Current date/time.

\- \*\*EXTRACT(YEAR/MONTH/DAY)\*\* → Pulls specific part of a date.

\- \*\*ADD\_MONTHS()\*\* → Adds months to a date.

\- \*\*MONTHS\_BETWEEN()\*\* → Difference in months between two dates.



📌 Time-based analysis is essential in business reporting (sales over time, employee tenure, etc.).



---



\## 🧠 Insights

\- Joins and subqueries are the backbone of SQL queries in data analysis.

\- Window functions are a \*\*game-changer\*\* — they simplify analytics.

\- String and date functions are crucial for \*\*data cleaning and reporting\*\*.



---



\## 🔗 Helpful Resources

\- \[W3Schools – SQL Joins](https://www.w3schools.com/sql/sql\_join.asp)  

\- \[Mode – SQL Window Functions](https://mode.com/sql-tutorial/sql-window-functions/)  

\- \[Oracle – SQL Functions](https://docs.oracle.com/en/database/)





---



\## 💻 Code Examples



\### 1️⃣ Joins



```sql

-- INNER JOIN: Only matching rows

SELECT e.emp\_id, e.name, d.department\_name

FROM employees e

INNER JOIN departments d ON e.department\_id = d.department\_id;



-- LEFT JOIN: All from employees, matched from departments

SELECT e.emp\_id, e.name, d.department\_name

FROM employees e

LEFT JOIN departments d ON e.department\_id = d.department\_id;



-- RIGHT JOIN: All from departments, matched from employees

SELECT e.emp\_id, e.name, d.department\_name

FROM employees e

RIGHT JOIN departments d ON e.department\_id = d.department\_id;



-- FULL OUTER JOIN: All rows from both tables

SELECT e.emp\_id, e.name, d.department\_name

FROM employees e

FULL OUTER JOIN departments d ON e.department\_id = d.department\_id;



-- SELF JOIN: Compare employees in the same department

SELECT a.name AS emp1, b.name AS emp2, a.department\_id

FROM employees a

JOIN employees b ON a.department\_id = b.department\_id

WHERE a.emp\_id <> b.emp\_id;

```



---



\### 2️⃣ UNION vs UNION ALL

```sql

-- UNION removes duplicates

SELECT department FROM employees

UNION

SELECT department FROM contractors;



-- UNION ALL keeps duplicates

SELECT department FROM employees

UNION ALL

SELECT department FROM contractors;

```



---



\### 3️⃣ Subqueries

```sql

-- Scalar Subquery

SELECT name, salary

FROM employees

WHERE salary > (SELECT AVG(salary) FROM employees);



-- IN with Subquery

SELECT name

FROM employees

WHERE department\_id IN (SELECT department\_id FROM departments WHERE location = 'New York');



-- Correlated Subquery

SELECT e1.name, e1.salary

FROM employees e1

WHERE e1.salary > (SELECT AVG(e2.salary) 

&nbsp;                  FROM employees e2 

&nbsp;                  WHERE e1.department\_id = e2.department\_id);

```



---



\### 4️⃣ Window Functions

```sql

-- Row numbering

SELECT name, ROW\_NUMBER() OVER (ORDER BY salary DESC) AS row\_num

FROM employees;



-- Ranking

SELECT name, RANK() OVER (ORDER BY salary DESC) AS rank\_num

FROM employees;



-- Dense Rank (no gaps)

SELECT name, DENSE\_RANK() OVER (ORDER BY salary DESC) AS dense\_rank\_num

FROM employees;



-- NTILE: Divide employees into 4 groups by salary

SELECT name, NTILE(4) OVER (ORDER BY salary DESC) AS quartile

FROM employees;



-- Lead \& Lag

SELECT name, salary,

&nbsp;      LAG(salary, 1) OVER (ORDER BY salary) AS prev\_salary,

&nbsp;      LEAD(salary, 1) OVER (ORDER BY salary) AS next\_salary

FROM employees;

```



---



\### 5️⃣ String Functions

```sql

SELECT UPPER(name) AS uppercase\_name,

&nbsp;      LOWER(name) AS lowercase\_name,

&nbsp;      SUBSTR(name, 1, 3) AS first\_three\_chars,

&nbsp;      TRIM('  John  ') AS trimmed\_name,

&nbsp;      CONCAT(name, ' works in ', department) AS full\_sentence

FROM employees;

```



---



\### 6️⃣ Date Functions

```sql

SELECT SYSDATE AS today,

&nbsp;      EXTRACT(YEAR FROM hire\_date) AS hire\_year,

&nbsp;      ADD\_MONTHS(hire\_date, 6) AS six\_months\_later,

&nbsp;      MONTHS\_BETWEEN(SYSDATE, hire\_date) AS months\_worked

FROM employees;

```



