# End-to-end analytics solution using Snowflake and PowerBI

This repository contains my full **end-to-end analytics project** built on top of the **Tasty Bytes** dataset.  
It demonstrates how I take raw data → integrate it with Marketplace data → model it → build a clean dimensional schema → and create insights using Power BI.

This project is structured exactly the way a real analytics/BI team would approach data modeling and dashboard development.

---

## 📁 Repository Structure

```
Snowflake-PowerBI-TastyBytes/
│
├─ index.md                        # GitHub Pages homepage (portfolio-style presentation)
├─ README.md                       # Repo overview
│
├─ sql/                            # All Snowflake SQL scripts used in the project
│   ├─ 1-data-profiling.sql
│   ├─ 2-marketplace-data.sql
│   ├─ 3-create-star-schema.sql
│   ├─ 4-data-governance.sql
│   └─ tasty-bytes-intro.sql
│
├─ data-model/
│   └─ fact_and_dimensions.md      # Detailed documentation of dimensions & fact tables
│
├─ pipelines/
│   └─ etl_pipeline.md             # Dynamic tables pipeline & ETL logic
│
├─ dashboards/
│   └─ insights.md                 # Power BI visuals & business insights
│
└─ assets/
    ├─ diagrams/                   # Architecture, lineage, and model diagrams
    │   ├─ snowflake_lineage.jpg
    │   ├─ powerbi_star_schema.jpg
    │   └─ powerbi_full_model.jpg
    └─ screenshots/                # Snowflake + Power BI screenshots
        ├─ snowflake_order_header_query.jpg
        └─ powerbi_dashboard.jpg
```

---

## 🚀 Project Overview

### **Objective**
Build an end-to-end analytics solution using:

- **Snowflake**  
- **Snowflake Marketplace**  
- **Dynamic Tables**  
- **Power BI**  

This project focuses on:

- Data profiling and quality checks  
- Creating a full **star schema** (dimensions + fact tables)  
- Using **dynamic tables** as a lightweight, CDC-friendly transformation layer  
- Exposing the curated dataset to Power BI  
- Producing insights using clean BI modeling  

---

## 🧱 Key Components

### 🔹 1. **Snowflake SQL & Data Engineering**
Located in the `/sql` folder.

Includes:

- Data profiling  
- Marketplace data setup  
- Dimensional modeling (surrogate keys, conformed dimensions)  
- Fact table creation  
- Data governance and schema/role setup  

These scripts collectively build:

- `DT_DIM_*` tables (Customers, Trucks, Locations, Dates, Times, Menu Items, Franchise)  
- `DT_FACT_ORDER_DETAIL`
- `DT_FACT_ORDER_HEADER`
- **`DT_FACT_ORDER_AGG`** – main analytics fact table  

---

### 🔹 2. **Dimensional Model Documentation**
Located in `/data-model/fact_and_dimensions.md`.

Contains:

- Grain definitions  
- Surrogate keys  
- Business attributes  
- Fact vs dimension logic  
- Complete star schema explanation  
- Model diagrams  

---

### 🔹 3. **ETL / Pipeline Logic**
Located in `/pipelines/etl_pipeline.md`.

Covers:

- How raw marketplace tables are mapped to dynamic tables  
- Refresh flow using Snowflake’s `TARGET_LAG`  
- Dependency graph & lineage  
- Warehouse assignments  
- Performance considerations  

---

### 🔹 4. **Power BI Dashboards & Insights**
Located in `/dashboards/insights.md`.

Includes:

- Screenshots of visuals  
- Regions → City performance analysis  
- KPI metrics using the aggregated fact table  
- Interpretation of insights  
- How data modeling enables faster reporting  

---

### 🔹 5. **Visual Assets**  
Located in `/assets`.

Contains:

- Architecture diagrams  
- Lineage screenshots  
- Power BI model views  
- SQL exploration screenshots  

These are also embedded into GitHub Pages for easier presentation.

---

## 🌐 GitHub Pages Portfolio
This repository is designed to be used as a **portfolio website**.

After enabling GitHub Pages:

```
Settings → Pages → Deploy from branch → main → root
```

Your portfolio will be available at:

```
https://yourusername.github.io/Snowflake-PowerBI-TastyBytes/
```

This page (index.md) presents the project like a case study with embedded diagrams, SQL samples, model views, and insights.

---

## 🎯 Skills Demonstrated

- Snowflake Marketplace data ingestion  
- Data profiling & quality checks  
- Dimensional modeling (facts & dimensions)  
- Dynamic tables in Snowflake  
- SQL transformations & aggregate fact design  
- Star schema modeling for BI  
- Power BI data modeling  
- KPI creation, slicers, cross-filters  
- Business insights summarization  
- Documentation & technical communication  

