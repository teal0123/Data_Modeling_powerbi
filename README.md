  Data Modeling & Architecture

### 🌟 Schema Design (Star Schema)
The data model is structured using a **Star Schema** to optimize query performance and enable scalable reporting:
- **Fact Table:** `Fact_Sales` (Contains transactional data, order quantities, revenue, and order dates).
- **Dimension Tables:** 
  - `Dim_Customer` (Customer profiles and demographics)
  - `Dim_Product` (Product categories, sub-categories, and unit prices)
  - `Dim_Date` (Custom Date Table for Time Intelligence analysis)

---

## 🧮 Custom DAX Functions & Measures

Key business metrics and calculations were created using advanced **DAX (Data Analysis Expressions)**:

### 1. Total Revenue
```dax
Total Revenue = SUM(Fact_Sales[Sales_Amount])
