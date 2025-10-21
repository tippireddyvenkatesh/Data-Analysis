\# Week 6 – Advanced Power BI (DAX \& Dashboard Design)



\## ✅ Topics Covered



\### 1️⃣ Advanced DAX Functions

DAX allows advanced calculations and context-based analysis.



\*\*Key DAX Categories:\*\*

\- \*\*Time Intelligence:\*\*  

&nbsp; `TOTALYTD()`, `SAMEPERIODLASTYEAR()`, `PARALLELPERIOD()`

\- \*\*Filter Functions:\*\*  

&nbsp; `CALCULATE()`, `FILTER()`, `ALL()`, `ALLEXCEPT()`, `REMOVEFILTERS()`

\- \*\*Iterators:\*\*  

&nbsp; `SUMX()`, `AVERAGEX()`, `COUNTX()` — perform calculations row by row

\- \*\*Context Functions:\*\*  

&nbsp; `VALUES()`, `SELECTEDVALUE()`, `HASONEVALUE()`



📌 Advanced DAX helps create KPIs, year-over-year comparisons, cumulative totals, and dynamic calculations.



---



\### 2️⃣ Dynamic Measures \& Conditional Formatting

Dynamic visuals respond to user selections.



\*\*Examples:\*\*

\- \*\*Dynamic Titles:\*\*

&nbsp; ```DAX

&nbsp; Title Measure = "Sales Report for " \& SELECTEDVALUE(DimDate\[Year], "All Years")



