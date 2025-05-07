# HR Analytics Project — SQL + Excel 📊

## 🔍 Overview
This project demonstrates basic HR analytics using SQL and Excel. It includes two datasets
- `Employees` — details about employees such as department, age, gender, salary, and employment status.
- `PerformanceReviews` — review scores and dates for employee performance evaluations.

The goal is to show how SQL and Excel can be used to extract insights from HR data.

---

## 🧰 Tools & Technologies
- SQL (for data creation, joins, filtering, aggregation)
- Microsoft Excel (for analysis, pivot tables, visualizations)
- CSV (as data source format)

---

## 📁 Files Included
- `employees.csv` synthetic employee data
- `performance_reviews.csv` synthetic performance review records
- (Optional) `analysis.xlsx` Excel file with charts and pivot tables (you can add your own)

---

## 🔍 Example Insights
- Average performance score by department
- Correlation between salary and performance
- Employee retention and attrition trends
- Age and gender distribution across departments

---

## 📝 How to Use
1. Import `employees.csv` and `performance_reviews.csv` into Excel or any SQL environment.
2. Use Power Query or pivot tables in Excel to analyze data.
3. Run SQL queries to explore relationships, group statistics, and trends.

---

## 📌 Sample SQL Queries
```sql
-- Average score per department
SELECT e.Department, AVG(p.Score) AS AvgScore
FROM Employees e
JOIN PerformanceReviews p ON e.EmployeeID = p.EmployeeID
GROUP BY e.Department;

-- Count of terminated employees
SELECT COUNT() AS Terminated
FROM Employees
WHERE TerminationDate IS NOT NULL;
