# 📊 Employee Attrition Analysis – Power BI Dashboard

This project explores the underlying factors contributing to employee attrition using a comprehensive dataset and presents insights through interactive visualizations built in **Power BI**.

## 📌 Project Overview

- 📁 **Tool Used:** Microsoft Power BI
- 📄 **Dataset Size:** 4,411 rows × 29 columns
- 📊 **Data Source:** Simulated HR dataset containing employee demographics, satisfaction levels, income, and attrition status

---

## 🎯 Objectives

1. Visualize employee attrition patterns by department, job level, age group, and salary.
2. Analyze correlations between attrition and various factors like job satisfaction, salary hike, and work-life balance.
3. Segment salaries into “Underpaid”, “Fairly Paid”, and “Overpaid” using custom DAX formulas.
4. Identify key drivers behind high attrition rates.
5. Build a Power BI dashboard to enable data-driven decisions for HR and leadership teams.

---

## 🧪 Methodology

- Cleaned dataset by removing irrelevant columns like `EmployeeCount`.
- Used multiple Power BI visuals: **Bar charts, Line charts, Treemaps, Pie charts, Heatmaps, and Pivot tables**.
- Created custom DAX measures to evaluate:
  - Job satisfaction trends over time
  - Salary segmentation by education level and department
  - Correlations between attrition and factors like job involvement, number of companies worked at, and performance rating

---

## 📈 Key Insights

- Departments with the highest attrition rates: **R&D (453 employees)**, followed by **Sales (201)** and **HR (57)**.
- Employees with **higher education levels** tend to report **greater job satisfaction**.
- **Job satisfaction and salary** have a high correlation with attrition.
- **HR employees** were found to be significantly underpaid, regardless of education level.
- Attrition is more prevalent among employees who have **worked at fewer companies** but are **underpaid** and report **lower satisfaction**.
- Performance rating shows a **linear relationship** with job involvement.

---

## 🧮 Sample DAX Formula

```DAX
Salary Status = SWITCH(TRUE(),
[Salary] < [Avg Salary], "Underpaid",
[Salary] = [Avg Salary], "Fairly Paid",
[Salary] > [Avg Salary], "Overpaid"
)
