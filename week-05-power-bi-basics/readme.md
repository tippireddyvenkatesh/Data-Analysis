---



\## 💻 Power BI Practice Examples



\### 1️⃣ Loading \& Transforming Data (Power Query)

\*\*Steps in Power Query:\*\*

1\. Go to \*\*Home → Get Data → Excel/CSV/SQL Server\*\*  

2\. Click \*\*Transform Data\*\* to open Power Query Editor  

3\. Use these key transformations:

&nbsp;  - Remove columns or duplicates  

&nbsp;  - Rename columns for clarity  

&nbsp;  - Change data types (Text, Number, Date)  

&nbsp;  - Merge two tables → `Home → Merge Queries`  

&nbsp;  - Append tables → `Home → Append Queries`  

&nbsp;  - Add new column → `Add Column → Custom Column`  



Example (Custom Column Formula):

```powerquery

= \[Sales] - \[Cost]

```

\*(Creates a “Profit” column in Power Query)\*



---



\### 2️⃣ Data Modeling Example

You have:

\- \*\*FactSales\*\* (SalesAmount, ProductKey, CustomerKey, DateKey)

\- \*\*DimProduct\*\* (ProductKey, ProductName, Category)

\- \*\*DimCustomer\*\* (CustomerKey, CustomerName, Region)

\- \*\*DimDate\*\* (DateKey, Date, Month, Year)



Create relationships:

\- FactSales\[ProductKey] → DimProduct\[ProductKey]

\- FactSales\[CustomerKey] → DimCustomer\[CustomerKey]

\- FactSales\[DateKey] → DimDate\[DateKey]



📌 Use \*\*Model View\*\* in Power BI Desktop to connect them.  

\*\*Star Schema\*\* → Fact table in the center, Dimension tables around it.



---



\### 3️⃣ DAX (Data Analysis Expressions)



\#### 🔹 Basic DAX Measures

```DAX

Total Sales = SUM(FactSales\[SalesAmount])

Average Sales = AVERAGE(FactSales\[SalesAmount])

Total Customers = DISTINCTCOUNT(FactSales\[CustomerKey])

```



\#### 🔹 Calculated Columns

```DAX

Profit = FactSales\[SalesAmount] - FactSales\[Cost]

Profit Margin = DIVIDE(FactSales\[Profit], FactSales\[SalesAmount], 0)

```



\#### 🔹 Logical \& Filter Functions

```DAX

High Sales = IF(FactSales\[SalesAmount] > 100000, "High", "Low")



Sales 2024 =

CALCULATE(

&nbsp;   SUM(FactSales\[SalesAmount]),

&nbsp;   FILTER(DimDate, DimDate\[Year] = 2024)

)

```



\#### 🔹 Time Intelligence

```DAX

Sales LY = CALCULATE(SUM(FactSales\[SalesAmount]), SAMEPERIODLASTYEAR(DimDate\[Date]))

YoY Growth = DIVIDE(\[Total Sales] - \[Sales LY], \[Sales LY])

```



---



\### 4️⃣ Visuals \& Dashboard Elements



| Visual Type | Used For | Example |

|--------------|-----------|----------|

| \*\*Bar / Column Chart\*\* | Compare categories | Sales by Region |

| \*\*Line Chart\*\* | Trends over time | Monthly Sales |

| \*\*Pie / Donut Chart\*\* | Proportion | Sales by Product Category |

| \*\*Card\*\* | KPIs | Total Revenue, Profit Margin |

| \*\*Map\*\* | Geographic Analysis | Sales by State |

| \*\*Matrix Table\*\* | Drill-down details | Product → Subcategory → Sales |

| \*\*Slicers\*\* | Interactive filters | Year, Region, Product |



📌 \*\*Tip:\*\* Use consistent colors and simple visuals for professional dashboards.



---



\### 5️⃣ Power BI Dashboard Publishing

\*\*Steps:\*\*

1\. Click \*\*Publish\*\* → Choose workspace  

2\. In \*\*Power BI Service\*\*, create dashboards using pinned visuals  

3\. Share securely via:

&nbsp;  - Workspace access  

&nbsp;  - Share link (with permissions)  

&nbsp;  - Power BI App for teams  



📌 \*\*Best Practice:\*\* Use Row-Level Security (RLS) if multiple users need restricted access.



---



\## 🧠 Key Takeaways

\- Power Query = Data Cleaning  

\- DAX = Calculations \& Analysis  

\- Model View = Relationships  

\- Report View = Visualization  

\- Power BI Service = Sharing Insights  



Together, these make Power BI a \*\*complete end-to-end data analysis tool\*\*.



