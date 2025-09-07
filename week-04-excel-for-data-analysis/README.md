\# Week 4 – Excel for Data Analysis



\## ✅ Topics Covered



\### 1. Excel Basics Refresher

\- Cells, rows, columns, worksheets

\- Formatting (number, text, currency, dates)

\- Conditional formatting to highlight data patterns



📌 Excel is the go-to tool for analysts and often the first step before moving into SQL/Python/BI tools.



---



\### 2. Functions \& Formulas

\- \*\*SUM, AVERAGE, COUNT, MAX, MIN\*\*

\- \*\*IF, AND, OR, NOT\*\* (logical functions)

\- \*\*VLOOKUP / HLOOKUP\*\* → Lookup values in tables

\- \*\*INDEX + MATCH\*\* → More powerful lookup than VLOOKUP

\- \*\*TEXT functions\*\* → LEFT, RIGHT, MID, TRIM, CONCAT, PROPER



📌 Functions let you clean, transform, and analyze raw data quickly.



---



\### 3. Data Cleaning Techniques

\- Removing duplicates

\- Handling blanks and errors (`IFERROR`)

\- Text-to-Columns

\- Data validation (drop-down lists)



📌 Clean data = reliable analysis.



---



\### 4. Pivot Tables \& Pivot Charts

\- Summarize large datasets quickly

\- Drag-and-drop fields for grouping, aggregations (SUM, COUNT, AVG)

\- Pivot charts to visualize summaries



📌 Pivot tables are a must-have skill for quick insights.



---



\### 5. Data Visualization

\- Creating bar, line, pie, scatter, histogram charts

\- Formatting charts for readability

\- Adding slicers for interactive filtering



📌 Visuals make insights easy to communicate.



---



\### 6. Advanced Excel Tools

\- \*\*Conditional Formatting with formulas\*\*

\- \*\*What-If Analysis\*\* → Goal Seek, Scenario Manager, Data Tables

\- \*\*Solver Add-In\*\* → Optimization problems

\- \*\*Named Ranges\*\* for cleaner formulas



📌 These tools move you beyond “basic Excel” into professional analytics.



---



\## 🧠 Insights

\- Excel remains the foundation tool for analysts despite advanced tools like SQL \& Python.

\- Mastering lookup functions, pivot tables, and data cleaning is more important than memorizing every formula.

\- Excel connects well with Power BI, making it a stepping stone into business intelligence.



---



\## 🔗 Helpful Resources

\- \[Excel Functions List – Microsoft](https://support.microsoft.com/en-us/office/excel-functions-alphabetical-b3944572-255d-4efb-bb96-c6d90033e188)  

\- \[Excel Jet – Formula Examples](https://exceljet.net/)





---



\## 💻 Excel Formula Examples



\### 1️⃣ Basic Functions

```excel

=SUM(A2:A10)         # Adds all numbers from A2 to A10

=AVERAGE(B2:B10)     # Finds average of values in B2 to B10

=COUNT(C2:C20)       # Counts numeric values in C2 to C20

=MAX(D2:D15)         # Returns highest value in D2:D15

=MIN(D2:D15)         # Returns lowest value in D2:D15

```



---



\### 2️⃣ Logical Functions

```excel

=IF(E2>5000, "High", "Low")                   # Categorize sales as High/Low

=AND(A2>50, B2="Yes")                         # Returns TRUE if both conditions match

=OR(A2="HR", A2="IT")                         # Returns TRUE if either condition is met

=NOT(A2="Finance")                            # Returns TRUE if value is not Finance

=IFERROR(1/0, "Error Found")                  # Returns "Error Found" instead of #DIV/0!

```



---



\### 3️⃣ Lookup Functions

```excel

=VLOOKUP(101, A2:D20, 3, FALSE)               # Finds employee ID 101 and returns 3rd column (e.g. Salary)

=HLOOKUP("Q1", A1:F4, 3, FALSE)               # Finds "Q1" across top row and returns 3rd row

=INDEX(B2:B10, 5)                             # Returns 5th value from range B2:B10

=MATCH(70000, C2:C20, 0)                      # Finds position of 70000 in range C2:C20

=INDEX(C2:C20, MATCH(70000, C2:C20, 0))       # Combines INDEX + MATCH for flexible lookups

```



---



\### 4️⃣ Text Functions

```excel

=UPPER(A2)          # Converts text to uppercase

=LOWER(B2)          # Converts text to lowercase

=PROPER(C2)         # Converts text to Proper Case (e.g. john doe → John Doe)

=LEFT(D2, 5)        # Extracts first 5 characters

=RIGHT(D2, 3)       # Extracts last 3 characters

=MID(D2, 2, 4)      # Extracts 4 characters starting from 2nd

=TRIM(E2)           # Removes extra spaces

=CONCAT(A2, " - ", B2)   # Combines values with a separator

```



---



\### 5️⃣ Pivot Table Examples

\*(Steps instead of formulas)\*  

1\. Select dataset → Insert → PivotTable  

2\. Drag `Department` → Rows  

3\. Drag `Salary` → Values → Change to \*\*Average\*\*  

4\. Drag `Gender` → Columns  

5\. Add Slicer for `Year` to filter interactively  



---



\### 6️⃣ Date Functions

```excel

=TODAY()                     # Returns today’s date

=NOW()                       # Returns current date + time

=YEAR(A2)                    # Extracts year from a date

=MONTH(A2)                   # Extracts month number

=DAY(A2)                     # Extracts day number

=TEXT(A2, "MMMM")            # Converts date to full month name

=EDATE(A2, 6)                # Adds 6 months to a given date

=DATEDIF(A2, B2, "Y")        # Finds years between two dates

```



---



\### 7️⃣ What-If Analysis

\- \*\*Goal Seek\*\* → Find input needed to reach a specific output  

\- \*\*Data Tables\*\* → See how results change for different inputs  

\- \*\*Scenario Manager\*\* → Compare multiple “what-if” situations  



---



\## 📊 Insights from Practice

\- VLOOKUP is great but INDEX+MATCH is more powerful.  

\- PivotTables are the fastest way to summarize big datasets.  

\- `IFERROR` is crucial for cleaning messy Excel outputs.  

\- Date \& text functions save a ton of time in data cleaning.  





