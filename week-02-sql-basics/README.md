# Week 2 – SQL Basics

## ✅ Topics Covered
- Creating and inserting data into tables
- SELECT statements
- WHERE clause for filtering
- ORDER BY to sort results
- DISTINCT to remove duplicates
- IN, BETWEEN, LIKE for advanced filtering
- IS NULL / IS NOT NULL checks
- Aliasing columns with AS
- FETCH FIRST n ROWS ONLY
- CASE WHEN for conditional logic
- GROUP BY for aggregation
- HAVING to filter grouped results

---

## 📘 What I Learned
- How to define tables and insert data into them
- Retrieving and filtering records using different SQL clauses
- Sorting and cleaning data using ORDER BY and DISTINCT
- Handling NULL values and renaming columns for clarity
- Using `CASE` for conditional categorization
- Aggregating data with functions like COUNT, AVG, MAX
- Grouping rows with GROUP BY and filtering with HAVING

---

## 🔧 Tools Used
- Oracle Live SQL
- GitHub for documentation

---

## 🧠 Insights
- Filtering with `WHERE` happens **before grouping**, `HAVING` is used **after**
- SQL is extremely powerful for cleaning, analyzing, and preparing data
- Small differences exist between SQL dialects (Oracle, MySQL, PostgreSQL)
- `CASE` statements are underrated and powerful for categorizing results
- Grouping and aggregation are essential for real-world business reports

---

## 🔗 Helpful Resources
- [SQL Tutorial – W3Schools](https://www.w3schools.com/sql/)
- [Oracle Live SQL](https://livesql.oracle.com/)
- [LeetCode SQL Practice](https://leetcode.com/problemset/database/)


---

## 💻 Code Examples

### 📌 1. Create Table
```sql
CREATE TABLE EMPLOYEES_TEST (
  emp_id INT,
  name VARCHAR(50),
  department VARCHAR(50),
  salary INT
);
```

### 📌 2. Insert Data
```sql
INSERT INTO EMPLOYEES_TEST (emp_id, name, department, salary)
VALUES (1, 'Alice', 'HR', 60000);

INSERT INTO EMPLOYEES_TEST (emp_id, name, department, salary)
VALUES (2, 'Bob', 'IT', 70000),
       (3, 'Carol', 'Finance', 65000),
       (4, 'David', 'IT', 72000),
       (5, 'Eve', NULL, 55000);
```

### 📌 3. Basic SELECT
```sql
SELECT * FROM EMPLOYEES_TEST;
```

### 📌 4. WHERE clause
```sql
SELECT * FROM EMPLOYEES_TEST WHERE department = 'IT';
```

### 📌 5. ORDER BY salary (descending)
```sql
SELECT * FROM EMPLOYEES_TEST ORDER BY salary DESC;
```

### 📌 6. DISTINCT values
```sql
SELECT DISTINCT department FROM EMPLOYEES_TEST;
```

### 📌 7. Filtering with IN, BETWEEN, LIKE
```sql
SELECT * FROM EMPLOYEES_TEST WHERE department IN ('IT', 'HR');
SELECT * FROM EMPLOYEES_TEST WHERE salary BETWEEN 60000 AND 70000;
SELECT * FROM EMPLOYEES_TEST WHERE name LIKE 'A%';
```

### 📌 8. NULL Handling
```sql
SELECT * FROM EMPLOYEES_TEST WHERE department IS NULL;
SELECT * FROM EMPLOYEES_TEST WHERE department IS NOT NULL;
```

### 📌 9. Aliasing Columns
```sql
SELECT name AS employee_name, salary AS income FROM EMPLOYEES_TEST;
```

### 📌 10. FETCH FIRST n ROWS
```sql
SELECT * FROM EMPLOYEES_TEST FETCH FIRST 3 ROWS ONLY;
```

### 📌 11. CASE WHEN Conditions
```sql
SELECT name, salary,
  CASE
    WHEN salary >= 70000 THEN 'High'
    WHEN salary BETWEEN 60000 AND 69999 THEN 'Medium'
    ELSE 'Low'
  END AS salary_band
FROM EMPLOYEES_TEST;
```

### 📌 12. Aggregation Functions
```sql
SELECT COUNT(*) FROM EMPLOYEES_TEST;
SELECT AVG(salary) FROM EMPLOYEES_TEST;
SELECT MAX(salary), MIN(salary) FROM EMPLOYEES_TEST;
```

### 📌 13. GROUP BY and HAVING
```sql
SELECT department, COUNT(*) AS total_employees
FROM EMPLOYEES_TEST
GROUP BY department
HAVING COUNT(*) > 1;
```

