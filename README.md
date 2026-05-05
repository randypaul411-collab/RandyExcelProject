# 📊 Data Cleaning & Analytics Pipeline (Power Query + Excel + SQL)

## 🚀 Project Overview
This project demonstrates a complete **data cleaning and transformation pipeline** using Power Query in Excel, designed to handle real-world messy operational data from a print & fabrication company (The Look Company-style dataset).

The goal is to transform raw, inconsistent data into a **clean, analysis-ready dataset** for downstream analytics and dashboarding (Power BI / SQL).

---

## 🎯 Objectives
- Clean and standardize messy real-world data
- Automate transformation using Power Query
- Prepare dataset for analytics and visualization
- Demonstrate end-to-end data workflow for portfolio

---

## 📁 Project Structure

---

## 🔧 Tools & Technologies

![Excel](https://img.shields.io/badge/Excel-PowerQuery-green)
![SQL](https://img.shields.io/badge/SQL-DataCleaning-blue)
![PowerBI](https://img.shields.io/badge/PowerBI-Dashboard-orange)
![Data](https://img.shields.io/badge/Data-Analytics-purple)

---

## 🧹 Data Cleaning Process (Power Query)

The dataset contained several real-world issues:

### ❌ Before Cleaning:
- Mixed date formats (`2022-01-01`, `01/02/2022`, `Jan 3, 2022`)
- Inconsistent text (`toronto`, `" Toronto "`)
- Product name inconsistencies (`Banner Print`, `banner print`)
- Null values in key fields
- Mixed data types (numbers stored as text)
- Price values with `$` symbols

---

### ✅ After Cleaning:
- Standardized date format (YYYY-MM-DD)
- Cleaned text (Trim, Clean, Proper Case)
- Normalized product names
- Converted data types correctly
- Removed unwanted characters (`$`, spaces)
- Structured dataset ready for analytics

---

## ⚙️ Key Power Query Transformations

- Text Cleaning:
  - `Text.Trim()`
  - `Text.Clean()`
  - `Text.Proper()`
---
- 📅Date Handling:
 - The dataset contained multiple date formats (e.g., `YYYY-MM-DD`, `DD/MM/YYYY`, `MMM DD, YYYY`).

 - To ensure accurate parsing, I used **locale-based conversion** in Power Query:

  - Applied regional settings during data type conversion
  - Used locale-aware parsing to correctly interpret ambiguous dates
  - Ensured consistent final format for analysis
---
### Example:
```powerquery
= Table.TransformColumnTypes(
    Source,
    {{"Order_Date", type date}},
    "en-GB"
)
```
---

- Data Type Fixing:
  - Number conversion
  - Currency cleaning

- Column Creation:
  - Revenue = Units Sold × Price per Unit
  - Delivery Time = Shipping Date – Order Date

---

## Analytical Use Cases

This cleaned dataset enables:

- Revenue analysis by:
  - Year
  - Province
  - Customer
  - Industry

- 🚚 Operational KPIs:
  - Delivery time tracking
  - Order volume trends

- 🏆 Business Insights:
  - Top customers (e.g., FIFA, Walmart)
  - Best-performing industries
  - Regional performance analysis

---

## 📂 Excel Model

📥 [Download Power Query Model](Excel/power-query-data-cleaning-model.xlsx)

---

## 🖼️ Power Query Workflow

![Power Query Steps](pq1.png)
![Power Query Steps](pq.png)

---

## Key Learnings

- Importance of structured data cleaning pipelines
- Handling inconsistent real-world data formats
- Automating repetitive data preparation tasks
- Preparing datasets for scalable analytics

---

## Next Steps

- Build Power BI dashboard
- Implement SQL-based transformation pipeline
- Optimize data model (Star Schema)
- Add automation with Python

---

## 👨‍💻 Author

**Paul Agbekpornu**  
MFI (Insurance & Data Science) – University of Toronto  

- 💼 Actuarial & Data Analytics  
- 📊 Power BI | SQL | Python | Excel  
- 🔗 Portfolio: https://randypaul411-collab.github.io/PaulRandytheAnalst.github.io/

---

## ⭐ If you like this project
Feel free to star ⭐ the repo and connect with me!
