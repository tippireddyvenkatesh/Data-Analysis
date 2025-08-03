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
s