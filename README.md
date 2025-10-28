# Sales Trend Analysis Using Aggregations

## 🎯 Objective
Analyze **monthly revenue and order volume** using SQL aggregations to uncover sales trends over time.

---

## 🛠️ Tools & Technologies
- **Database:** SQLite (compatible with PostgreSQL / MySQL)
- **Language:** SQL
- **Data Source:** `online_sales_cleaned.csv`
- **Database File:** `online_sales.db`
- **Table Name:** `orders`

---

## 📂 Dataset Description

The dataset contains information on online sales transactions, including product details, order date, quantity, and price.

### Key Columns:
| Column | Description |
|--------|--------------|
| InvoiceNo | Unique identifier for each order |
| InvoiceDate | Date and time of the order |
| Category | Product category |
| Quantity | Number of units sold |
| UnitPrice | Price per unit |
| TotalAmount | Computed as `Quantity * UnitPrice` |
| Country | Customer's country |

---

## 🧹 Data Cleaning Process

1. **Removed invalid rows** with negative or zero `Quantity` or `UnitPrice`.  
2. **Converted `InvoiceDate`** to proper datetime format.  
3. **Created `TotalAmount`** = `Quantity * UnitPrice`.  
4. **Dropped unnecessary columns** to focus on sales data.  
5. **Sampled 2,000 records** from the original dataset (49,782 rows) for lightweight analysis.  
6. **Saved cleaned data** as:
   - `online_sales_cleaned.csv`
   - `online_sales.db` (SQLite database)

---

## 🧩 SQL Table Schema

**Table Name:** `orders`

| Column | Data Type |
|--------|------------|
| InvoiceNo | INTEGER |
| InvoiceDate | TEXT |
| Category | TEXT |
| Quantity | INTEGER |
| UnitPrice | REAL |
| TotalAmount | REAL |
| Country | TEXT |

---

📈 Expected Insights

Identify peak months and seasons for revenue.

Compare yearly revenue growth trends.

Determine top-performing categories and countries.

Analyze average order values over time.

Understand quarterly (seasonal) performance.

## 📊 Example Output Preview

| Year | Month | Total_Revenue | Total_Orders |
|------|--------|----------------|---------------|
| 2020 | 01 | 122,500 | 95 |
| 2020 | 02 | 133,450 | 110 |
| 2020 | 03 | 125,780 | 102 |
| 2020 | 04 | 138,920 | 108 |
| 2020 | 05 | 142,310 | 115 |
| 2020 | 06 | 129,870 | 98 |
| 2020 | 07 | 144,560 | 121 |
| 2020 | 08 | 139,240 | 117 |

📦 Deliverables

online_sales_cleaned.csv — Cleaned dataset

online_sales.db — SQLite database file

sales_trend_analysis.sql — SQL script with all 10 queries

PDF / Screenshot — Query results summary (for submission/report)
