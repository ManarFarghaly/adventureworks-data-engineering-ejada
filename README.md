# AdventureWorks Data Engineering & BI Pipeline (Ejada Internship)

## Overview
This project delivers an end-to-end **Data Engineering and Business Intelligence solution** for AdventureWorks Cycles, developed during my Data & Analytics internship.

It transforms transactional (OLTP) data into a high-performance analytical (OLAP) system, enabling faster insights and data-driven decision-making.

---

## Problem Statement
The original OLTP system was not optimized for analytics:
- Slow query performance for reporting
- No historical tracking of changes
- Difficulty generating unified insights across data sources

---

## Data Engineering Solution

### Data Warehouse Design
- Designed a **Star Schema** (Fact & Dimension tables)
- Implemented **Columnstore Indexes** for high-performance queries
- Applied **Slowly Changing Dimensions (SCD Type 1 & Type 2)** for historical tracking
- Offloaded reporting from OLTP to improve system performance

---

### ETL Pipeline (SSIS)
- Built a **dynamic, parameterized ETL pipeline**
- Supported:
  - Initial Load
  - Incremental Load (Watermarking approach)
- Introduced a **Staging Layer** for validation and buffering

#### Transformations:
- Lookups
- Conditional Splits
- Derived Columns
- SCD logic implementation

#### Additional Handling:
- Surrogate key generation
- Metadata tracking
- Constraint management for smooth automation

---

## Business Intelligence Solution

Built using Power BI on top of the Data Warehouse:

### KPI Dashboard
- Revenue, Cost, Profit, Profit Margin
- Orders, Customers, Products
- Active Customer Ratio

### Analytics Features
- Time-based analysis (MoM & YoY)
- Customer behavior insights
- Product performance tracking
- Shipping efficiency analysis

### Interactivity
- Drill-through pages (Customers, Orders, Products)
- Dynamic filters and slicers
- Interactive visuals and maps

---

## Tech Stack
- Microsoft SQL Server (OLTP + Data Warehouse)
- SSIS (SQL Server Integration Services)
- Power BI
- SQL & DAX

---

## Results
- Achieved up to **3× faster query performance** (OLAP vs OLTP)
- Built a **scalable and maintainable data pipeline**
- Delivered a **unified dashboard** replacing static reports
- Enabled faster, data-driven business decisions

---

## Project Structure

├── data-warehouse/

│ ├── schema.sql

│ └── tables/

├── etl/

│ ├── ssis-packages/

│ └── scripts/

├── powerbi/

│ └── dashboard.pbix

├── docs/

│ ├── architecture.png

│ └── pipeline.png

└── README.md

---

## Key Highlights
- End-to-end pipeline (Data Engineering → BI)
- Incremental ETL using watermarking
- Historical tracking using SCD
- Performance optimization using columnstore indexing

---

## Notes
- Dataset: AdventureWorks
- This project was developed for learning and demonstration purposes during an internship.

---

## Acknowledgment
Special thanks to my mentors for their guidance and support throughout this project.
