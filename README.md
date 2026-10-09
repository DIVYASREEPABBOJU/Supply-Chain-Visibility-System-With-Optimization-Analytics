

```markdown
# Supply Chain Visibility System With Optimization Analytics

## 📌 Project Overview

The **Supply Chain Visibility System With Optimization Analytics** is a Power BI-based analytics project developed to provide interactive insights into vessel movement, shipment performance, inventory, transportation, delivery, and warehouse operations.

The project uses **AIS vessel-tracking data enriched with weather information** and develops a series of Power BI dashboards across four milestones. The solution applies data modelling, Power Query, DAX, KPI analysis, and interactive visualizations to support data-driven supply chain decision-making.

---

## 🎯 Objectives

- Analyse vessel and shipment movement patterns
- Monitor supply chain and fleet performance
- Analyse inventory and delivery-related metrics
- Evaluate supplier and transportation performance
- Analyse warehouse efficiency and operational performance
- Develop executive-level dashboards for decision-making
- Provide interactive supply chain insights using Power BI
- Support data-driven supply chain optimization

---

## 🛠️ Tools & Technologies

- Power BI Desktop
- Power Query
- DAX
- Star Schema Data Modelling
- Data Visualization
- Python
- Pandas
- NumPy
- AIS Vessel Data
- Weather Data

---

# 📊 Project Milestones

## Milestone 1 – Data Modelling & KPI Foundation

The first milestone focuses on building the basic supply chain analytics model and establishing key performance indicators.

### Key Activities

- Data preparation and transformation using Power Query
- Creation of fact and dimension tables
- Development of a star-schema data model
- Creation of DAX measures
- Analysis of vessel movement and fleet performance
- Weather impact analysis
- Development of interactive KPI dashboards

### Key KPIs

- Total Vessels
- Total Pings
- Average Speed
- Average Transit Distance
- Average ETA
- Fleet Utilization Rate
- Cargo Throughput Velocity
- Delayed Trips %
- Weather-Impacted Trips %

---

## Milestone 2 – Inventory & Delivery Analytics

The second milestone extends the model to inventory and delivery-related analytics.

### Key Activities

- Inventory analysis
- Delivery performance analysis
- Product and warehouse-level analysis
- Slow-moving product identification
- Delivery trend and variance analysis
- Interactive drill-down analysis

### Key Metrics

- Total Inventory
- Total Products
- Slow-Moving Products
- Total Shipments
- Delivery Performance
- Transit and ETA Analysis

---

## Milestone 3 – Supplier & Transportation Analytics

The third milestone focuses on transportation and supplier-related performance.

### Key Activities

- Supplier performance analysis
- Transportation cost analysis
- Shipment analysis
- Route and warehouse analysis
- Fulfillment and quality analysis
- Development of transportation KPIs

### Key Metrics

- Total Transportation Cost
- Average Shipment Cost
- Total Shipments
- Fulfillment Rate
- On-Time Rate
- Quality Score

> **Note:** The original AIS dataset does not contain dedicated supplier, carrier, or transportation-cost fields. Proxy mappings and an assumed transportation cost rate were used for analytical purposes.

---

# Milestone 4 – Warehouse & Executive Analytics

Milestone 4 extends the existing model into warehouse efficiency, executive analysis, and performance optimization.

The dataset does not contain dedicated order IDs, physical warehouse capacity, picking transactions, or physical shipped-quantity fields. Therefore, proxy measures were developed using available shipment, vessel movement, delay, distance, and ETA fields.

---

## 📌 Data Model

The Power BI model follows a **Star Schema** consisting of:

### Fact Table

- `Fact_Shipment`

### Dimension Tables

- `Dim_Product`
- `Dim_Warehouse`
- `Dim_Status`
- `Dim_Date`

### Measures Table

- `_Measures`

---

## 📈 Milestone 4A – Warehouse Efficiency Report

The Warehouse Efficiency Report provides detailed operational analysis of warehouse performance.

### KPI Cards

- Total Orders
- Total Shipped Quantity
- Capacity Utilisation
- On-Time Delivery
- Picking Accuracy
- Operating Cost

### Visualizations

- Total Order Quantity by Warehouse
- Capacity Utilisation by Warehouse
- Picking Accuracy by Warehouse
- Total Orders by Zone
- Average On-Time Delivery by Warehouse
- Average Processing Hours by Warehouse
- Total Product Category

---

## 📊 Milestone 4B – Executive Overview

The Executive Overview dashboard provides a high-level view of supply chain performance for management and decision-making.

### KPI Cards

- Total Orders
- Total Shipped Quantity
- Capacity Utilisation
- On-Time Delivery
- Picking Accuracy
- Operating Cost

### Interactive Filters

- Date
- Warehouse
- Zone
- Order Type

### Visualizations

- Total Orders by Date
- Total Orders by Warehouse
- Total Inventory by Warehouse
- On-Time Delivery by Warehouse
- Picking Accuracy by Warehouse

---

## ⚙️ Milestone 4C – Performance Optimization

The Performance Optimization dashboard provides a consolidated warehouse-level comparison.

### Key Metrics

- Warehouse City
- Capacity Utilisation
- On-Time Delivery
- Picking Accuracy
- Processing Hours

This view helps identify warehouses with comparatively higher or lower operational performance.

---


---

# 🔄 Data Preparation

Power Query was used for data preparation and transformation activities including:

- Data cleaning
- Data type transformation
- Column preparation
- Date and time extraction
- Derived field creation
- Data standardization
- Preparation of fact and dimension tables

---

# 🗂️ Repository Structure

```text
Supply-Chain-Visibility-System-With-Optimization-Analytics/
│
├── Document/
│   └── Infosys_Internship_Supply_Chain_Visibility_Project_Updated_Report.pdf
│
├── PowerBI/
│   ├── Infos Milestone 1 Completion File.pbix
│   ├── Infos Milestone 2 Completion File.pbix
│   ├── Infos Milestone 3 Completion File.pbix
│   ├── Infos Milestone 4A Completion File.pbix
│   ├── Infos Milestone 4B Completion File.pbix
│   └── Infos Milestone 4C Completion File.pbix
│
├── Screenshots/
│   ├── Data Model.png
│   ├── Milestone 1.png
│   ├── Milestone 2.png
│   ├── Milestone 3.png
│   ├── Milestone 4A.png
│   ├── Milestone 4B.png
│   └── Milestone 4C.png
│
├── LICENSE
└── README.md
```

---

# 🖼️ Dashboard Screenshots

## Data Model – Star Schema

![Data Model](Screenshots/Data%20Model.png)

## Milestone 1

![Milestone 1](Screenshots/Milestone%201.png)

## Milestone 2

![Milestone 2](Screenshots/Milestone%202.png)

## Milestone 3

![Milestone 3](Screenshots/Milestone%203.png)

## Milestone 4A – Warehouse Efficiency

![Milestone 4A](Screenshots/Milestone%204A.png)

## Milestone 4B – Executive Overview

![Milestone 4B](Screenshots/Milestone%204B.png)

## Milestone 4C – Performance Optimization

![Milestone 4C](Screenshots/Milestone%204C.png)

---

# 📄 Project Report

The complete project and internship report covering all four milestones is available in the `Document` folder.

**Report:**  
`Infosys_Internship_Supply_Chain_Visibility_Project_Updated_Report.pdf`

---

# ⚠️ Data & Proxy Metric Note

The original AIS vessel-tracking dataset does not contain dedicated fields for certain traditional warehouse and supply-chain measures such as physical warehouse capacity, order IDs, picking transactions, and physical shipped quantity.

Therefore, proxy mappings were used for Milestone 4:

| Business Metric | Proxy Used |
|---|---|
| Total Orders | Unique MMSI + destination cluster combinations |
| Total Shipped Quantity | Shipment distance (`dist_km`) |
| Capacity Utilisation | Moving shipment records |
| On-Time Delivery | Delay status |
| Picking Accuracy | On-Time Delivery proxy |
| Operating Cost | Distance × assumed $2.50/km |
| Processing Hours | Average ETA hours |

These mappings were used to demonstrate analytical and dashboard-development capabilities using the available dataset.

---

# 📌 Key Outcomes

The project demonstrates how Power BI can be used to transform operational data into interactive supply chain analytics.

The completed solution provides:

- Data modelling using a star schema
- Data transformation using Power Query
- KPI development using DAX
- Interactive dashboards
- Inventory and delivery analysis
- Transportation and supplier analysis
- Warehouse efficiency analysis
- Executive-level performance monitoring
- Comparative warehouse performance analysis

---

# 👩‍💻 Author

**Divya Sree Pabboju**



---

# 📜 License

This project is licensed under the **MIT License**.

See the [LICENSE](LICENSE) file for details.
```

**To update it:** open your repository → `README.md` → click the **pencil/edit icon** → select all existing text → paste the code above → **Commit changes**.
