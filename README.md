# shield-insurance-powerbi-dashboard

# 🛡️ Shield Insurance - Power BI Dashboard

A multi-page interactive Power BI dashboard built as part of the **Codebasics Virtual Internship**, analyzing insurance policy data across customer demographics, sales channels, and revenue trends.

---

## 📊 Live Dashboard
🔗 [View Live Dashboard](https://app.powerbi.com/view?r=eyJrIjoiY2VjZDM3MzEtYzEyYy00ZWY3LWJhMjQtNGU0MmM2ZjZjMjU5IiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)

## 🎥 Video Walkthrough
🔗 [Watch on LinkedIn](https://www.linkedin.com/posts/sushant-bhusal-5b151b239_powerbi-dataanalytics-dashboard-activity-7463935433836515328-q3Q-?utm_source=share&utm_medium=member_desktop&rcm=ACoAADtX6pUBQCeXCvIvL18BvEh5YEgtY89F7BE)

---

## 🧩 Problem Statement

Shield Insurance needed a centralized interactive dashboard to monitor revenue performance, customer acquisition, and policy trends across cities, age groups, and sales modes — enabling data-driven business decisions.

---

## 📁 Data Model

The dashboard is built on 5 tables:

| Table | Type | Description |
|---|---|---|
| `fact_premiums` | Fact | Policy transactions — date, customer, policy, sales mode, premium amount |
| `fact_settlements` | Fact | Settlement % by age (standalone table) |
| `dim_customer` | Dimension | Customer info — customer code, DOB, city |
| `dim_date` | Dimension | Date table — daily, monthly, week-level data |
| `dim_policies` | Dimension | Policy info — policy ID, base cover, base premium |

---

## 📐 DAX Measures

| Measure | Description |
|---|---|
| Total Revenue | Sum of all final premium amounts |
| Total Customers | Distinct count of customers |
| Daily Revenue Growth (DRG) | Average daily revenue within selected period |
| Daily Customer Growth (DCG) | Average daily customers within selected period |
| Total Revenue LM % | Month-over-Month % change in revenue |
| Total Customers LM % | Month-over-Month % change in customers |
| Daily Revenue Growth LM % | LM % change for DRG |
| Daily Customer Growth LM % | LM % change for DCG |

---

## 🔧 Calculated Columns

| Column | Table | Description |
|---|---|---|
| Age | dim_customer | Derived from date of birth |
| Age Group | dim_customer | Segmented into 18-24, 25-30, 31-40, 41-50, 51-65, 65+ |
| Age Group | fact_settlements | Same segmentation applied to settlements table |
| Month Year | dim_date | Formatted as MMM YY for visual display |
| Month Sort | dim_date | Numeric key to sort months chronologically |

---

## 📋 Dashboard Pages

### Page 1 — General View
- KPI cards: Total Revenue, Total Customers, Daily Revenue Growth, Daily Customer Growth (with LM % reference labels)
- Monthly revenue/customer trend line chart with toggle
- Revenue & Customer split tables by City and Age Group
- City → Age Group drilldown matrix
  
![General View](General%20View.png)

### Page 2 — Sales Mode Analysis
- Treemap: Total Revenue and Total Customers split by sales mode
- Line chart: Sales mode trend over months

![Sales Mode](Sales%20Mode.png)

### Page 3 — Age Group Analysis
- Clustered bar: Age Group vs Policy Preference
- Line chart: Trend by Age Groups over months
- 100% Stacked bar: Age Group vs Sales Mode
- Line chart: Age Group vs Expected Settlements
- Bar chart: Total Customers by Age Group

![Age Group](Age%20Group.png)

---

## 🛠️ Tools Used

- **Power BI Desktop** — Dashboard development
- **Power Query (M)** — Data transformation and calculated columns
- **DAX** — Measures and KPI calculations
- **GitHub** — Version control and project sharing

---

## 🏅 Internship

This project was completed as part of the **Codebasics Virtual Internship** a 1-month program focused on real-world data analytics projects.

---

## 📬 Connect

Feel free to connect with me on [LinkedIn](#) <!-- Replace with your LinkedIn profile link -->
