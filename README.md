#  Swiggy Data Analysis using SQL

##  Project Overview

This project focuses on analyzing Swiggy food delivery data using Microsoft SQL Server. The objective is to clean, transform, and analyze the dataset to identify meaningful insights related to customer orders, revenue, restaurants, food categories, dishes, and geographical performance.

The project demonstrates practical SQL skills, including data validation, data cleaning, duplicate removal, database normalization, indexing, table creation, joins, aggregate functions, Common Table Expressions (CTEs), and business performance analysis.

A **Star Schema Data Model** is designed to organize the data into dimension tables and a fact table, making analytical queries more efficient and structured.

---

##  Project Objectives

- Perform data validation and identify missing values.
- Detect and remove duplicate records.
- Identify blank or empty string values.
- Create dimension tables and a fact table.
- Transform the raw dataset into a structured Star Schema.
- Analyze order trends across different time periods.
- Identify top-performing cities and restaurants.
- Analyze revenue contribution by state.
- Understand popular food categories and dishes.
- Generate key performance indicators (KPIs).

---

##  Technologies & Tools Used

- **Microsoft SQL Server** – Database management and query execution.
- **SQL (T-SQL)** – Data cleaning, transformation, and analysis.
- **SQL Server Management Studio (SSMS)** – Writing and executing SQL queries.
- **CSV Dataset** – Source data for the analysis.
- **GitHub** – Project documentation and version control.

---

##  1. Data Cleaning & Validation

The raw Swiggy dataset was checked and cleaned before performing analysis.

The following operations were performed:

- **NULL Value Detection:** Identified missing values in important columns using `IS NULL`.
- **Blank Value Detection:** Checked empty string values using `''`.
- **Duplicate Detection:** Identified duplicate records using `GROUP BY` and `HAVING COUNT(*) > 1`.
- **Duplicate Removal:** Removed duplicate records using a CTE and `ROW_NUMBER()`.

---

##  2. Data Transformation

The raw dataset was transformed into a structured **Star Schema** to improve data organization and analytical efficiency.

### Database Schema

The project consists of five dimension tables and one fact table.

**Dimension Tables:**

| Table Name | Description |
|---|---|
| Date_Table | Stores date-related information such as year, month, quarter, and week. |
| Location_Table | Stores state, city, and location details. |
| Restaurant_Table | Stores unique restaurant names. |
| Category_Table | Stores unique food categories. |
| Dish_Table | Stores unique dish names. |

**Fact Table:**

| Table Name | Description |
|---|---|
| Swiggy_Orders | Stores order-related measures such as price, rating, rating count, and foreign keys. |

### Star Schema Structure

The fact table is connected to all five dimension tables using primary keys and foreign keys.

This structure helps organize data and perform analytical queries efficiently.

---

## 3. Key Performance Indicators (KPIs)

The following KPIs were calculated using SQL:

1. **Total Orders** – Calculates the total number of orders.
2. **Total Revenue** – Calculates the overall revenue generated.
3. **Average Dish Price** – Calculates the average price of dishes.

---

##  4. Data Analysis & Business Insights

The project includes the following SQL analysis:

### A. Time-Based Analysis

- Monthly Order Analysis
- Monthly Revenue Analysis
- Quarterly Order Analysis
- Yearly Order Analysis
- Weekday Order Analysis

### B. Geographical Analysis

- Top 10 Cities by Orders
- Bottom 5 Cities by Orders
- Revenue Contribution by State

### C. Restaurant & Food Analysis

- Top 10 Restaurants by Orders
- Food Categories by Total Orders
- Top 10 Most Ordered Dishes
- Average Rating by Food Category

### D. Price-Based Analysis

- Order Distribution by Price Range:
  - Under ₹100
  - ₹100–₹199
  - ₹200–₹299
  - ₹300–₹399
  - ₹400–₹499
  - ₹500 and above

---

##  5. SQL Concepts Used

This project demonstrates the practical application of the following SQL concepts:

- SELECT and WHERE
- CREATE TABLE and DROP TABLE
- CREATE INDEX
- IS NULL and empty string checks
- GROUP BY and HAVING
- ORDER BY
- COUNT(), SUM(), AVG()
- CASE WHEN
- INNER JOIN
- Common Table Expressions (CTE)
- ROW_NUMBER()
- Primary Keys and Foreign Keys
- INSERT INTO SELECT
- DATEPART(), DATENAME(), YEAR(), MONTH(), DAY()
- CONVERT() and FORMAT()

---


## 7. How to Run This Project

**Step 1 – Create the Database**

```sql
CREATE DATABASE Swiggy;
GO

USE Swiggy;
GO
```

**Step 2 – Import the Dataset**

Import the Swiggy CSV dataset into SQL Server and create the `Swiggy_Data` table.

**Step 3 – Perform Data Cleaning**

Execute the SQL queries for NULL checks, blank value detection, duplicate identification, and duplicate removal.

**Step 4 – Create the Star Schema**

Create the five dimension tables and the `Swiggy_Orders` fact table.

**Step 5 – Insert Data**

Populate the dimension tables and fact table using `INSERT INTO SELECT` statements and appropriate JOIN conditions.

**Step 6 – Perform Data Analysis**

Execute the KPI and analytical queries to explore order trends, revenue, restaurant performance, food categories, and geographical insights.

---

##  8. What I Learned

Through this project, I gained practical experience in:

- Cleaning and validating real-world datasets using SQL.
- Handling NULL values, blank strings, and duplicate records.
- Designing a Star Schema using fact and dimension tables.
- Understanding relationships between tables using primary and foreign keys.
- Writing SQL queries for business analysis.
- Calculating KPIs and analyzing business performance.
- Performing time-based, geographical, restaurant, and price-based analysis.
- Improving SQL skills through practical data analytics tasks.

---

##  Author

**Arti Gautam**  
Aspiring Data Analyst | SQL | Microsoft SQL Server | Data Analysis
