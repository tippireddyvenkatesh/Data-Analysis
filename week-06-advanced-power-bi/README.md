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


---

## 💻 Advanced Power BI – Practical Examples

### ✅ 1️⃣ Advanced DAX Measures

**Year-to-Date (YTD) Sales**
```DAX
Sales YTD =
TOTALYTD(
    SUM(FactSales[SalesAmount]),
    DimDate[Date]
)
```

**Last Year’s Sales for YoY comparison**
```DAX
Sales LY =
CALCULATE(
    SUM(FactSales[SalesAmount]),
    SAMEPERIODLASTYEAR(DimDate[Date])
)
```

**Year-over-Year Growth**
```DAX
YoY Growth =
DIVIDE([Sales YTD] - [Sales LY], [Sales LY], 0)
```

**Profit Margin**
```DAX
Profit Margin =
DIVIDE([Total Profit], [Total Sales], 0)
```

---

### ✅ 2️⃣ Dynamic Titles (Interactive Reporting)
```DAX
Dynamic Title =
"Sales Performance for " &
SELECTEDVALUE(DimDate[Year], "All Years")
```

📌 This updates chart titles based on slicer selections.

---

### ✅ 3️⃣ Conditional Formatting for KPI Alerts

```DAX
Profit Status =
IF([Profit Margin] > 0.20, "Good",
    IF([Profit Margin] > 0.10, "Average", "Poor")
)
```

Then use this field to **color code KPIs**:
- Green → Good  
- Yellow → Average  
- Red → Poor  

---

### ✅ 4️⃣ Time Intelligence with Custom Periods
```DAX
Sales Last 30 Days =
CALCULATE(
    [Total Sales],
    DATESINPERIOD(DimDate[Date], MAX(DimDate[Date]), -30, DAY)
)
```

📌 Useful for recent activity dashboards.

---

### ✅ 5️⃣ Tooltips, Drillthrough & Bookmarking

| Feature | Usage | Example |
|--------|-------|---------|
| **Tooltips** | Show extra info on hover | Profit breakdown on charts |
| **Drillthrough** | Right-click to filter details | View selected Region → Stores |
| **Bookmarks** | Save report states | Before & after filters view |

📌 These improve storytelling and user experience.

---

### ✅ 6️⃣ Performance Optimization Examples

| Issue | Fix |
|------|-----|
| Slow visuals | Use **Performance Analyzer** |
| Large model | Remove unused columns |
| Complex calculations | Replace columns with **measures** |
| High data refresh time | Use aggregated summarization tables |

---

## 🔥 Best Dashboard Layout Tip (BI Design Rule)

📌 **Place visuals in this order**:

1️⃣ Top row → KPIs (Sales, Profit, YoY Growth)  
2️⃣ Middle row → Trends (Line chart)  
3️⃣ Bottom row → Breakdown (Bar/Map tables)  
4️⃣ Left side → Filters/Slicers  

✅ Clear storytelling path: **Summary → Trend → Detail**

---

## ✅ Summary
| Feature | Value |
|--------|------|
| Dynamic visuals | ✅ |
| Performance tuned | ✅ |
| Professional reporting | ✅ |

---

🚀 End of Week 6 Practical Section — You now understand **enterprise-level Power BI skills**!



