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



