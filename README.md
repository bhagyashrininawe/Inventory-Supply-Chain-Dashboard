# 📦 Inventory & Supply Chain Dashboard

A fully interactive **Inventory & Supply Chain Dashboard** developed using **Microsoft Excel, Power Query, and Power Pivot** to monitor inventory levels, track stock movements, identify low stock items, and support data-driven operational decision-making through dynamic reporting and visualizations.

---

## 🔥 Project Highlights

- ✔ Cleaned and transformed **2,000+ inventory records** using Power Query
- ✔ Performed inventory data validation and quality checks
- ✔ Developed interactive KPI dashboards for stock monitoring
- ✔ Built DAX measures using Power Pivot for inventory reporting
- ✔ Analyzed warehouse performance and inventory distribution
- ✔ Identified low stock products requiring replenishment
- ✔ Designed dynamic dashboards using Pivot Charts, Slicers, and Timelines

---

## 🧠 Skills & Tools Used

### 📌 Microsoft Excel
- Advanced Excel
- Pivot Tables
- Pivot Charts
- Conditional Formatting
- Dashboard Development
- Data Validation

### 📌 Power Query
- Data Cleaning
- Remove Duplicates
- Data Transformation
- Handle Null Values
- Standardize Category Names
- Data Quality Validation

### 📌 Power Pivot
- Data Modeling
- DAX Measures
- KPI Calculations
- Relationship Management

### 📌 Inventory Analytics
- Inventory Value Analysis
- Stock Monitoring
- Reorder Analysis
- Warehouse Performance Analysis
- Supplier Analysis
- Inventory Trend Analysis

---

## 🗂 Dashboard Screenshot

<img width="934" height="425" alt="Screenshot 2026-06-12 095604" src="https://github.com/user-attachments/assets/034bb505-9bd0-45dc-8acd-948c5f9fbb93" />


---

## 📈 Dashboard Features

### ➤ Inventory Overview
- Total Inventory Value
- Total Products
- Total Stock Quantity
- Low Stock Items
- Average Unit Cost

### ➤ Inventory Analysis
- Inventory by Category
- Inventory Value by Warehouse
- Top Products by Sales Quantity

### ➤ Stock Monitoring
- Low Stock Alert Report
- Reorder Analysis
- Stock Movement Tracking

### ➤ Supplier Insights
- Supplier-wise Inventory Distribution
- Supplier Performance Analysis

### ➤ Trend Analysis
- Monthly Stock Movement
- Quarterly Inventory Trends

### ➤ Interactive Filters
- Category Slicer
- Warehouse Slicer
- Supplier Slicer
- Timeline Filter

---

## 📊 DAX Measures Used

### Total Inventory Value

```DAX
Total Inventory Value :=
SUMX(
    Inventory,
    Inventory[Closing Stock] * Inventory[Unit Cost]
)
```

### Total Products

```DAX
Total Products :=
DISTINCTCOUNT(
    Inventory[SKU ID]
)
```

### Total Stock

```DAX
Total Stock :=
SUM(
    Inventory[Closing Stock]
)
```

### Average Unit Cost

```DAX
Average Unit Cost :=
AVERAGE(
    Inventory[Unit Cost]
)
```

### Total Sold Quantity

```DAX
Total Sold Qty :=
SUM(
    Inventory[Sold Qty]
)
```

### Low Stock Flag (Calculated Column)

```DAX
Low Stock Flag =
IF(
    Inventory[Closing Stock] <= Inventory[Reorder Level],
    "Yes",
    "No"
)
```

### Low Stock Items

```DAX
Low Stock Items :=
CALCULATE(
    DISTINCTCOUNT(
        Inventory[SKU ID]
    ),
    Inventory[Low Stock Flag] = "Yes"
)
```

---

## 🧩 Data Cleaning & Transformation Performed

- Removed duplicate SKU IDs
- Standardized category names
- Handled blank supplier values
- Investigated negative stock values
- Validated reorder levels
- Created Low Stock Flag
- Created Month, Year, and Quarter columns
- Performed inventory data quality checks

---

## 🗂 Dataset Information

The dataset contains **2,000 inventory records** with real-world data quality issues to simulate operational reporting scenarios.

### Dataset Columns

- SKU ID
- Product Name
- Category
- Supplier
- Warehouse
- Opening Stock
- Received Qty
- Sold Qty
- Closing Stock
- Reorder Level
- Unit Cost
- Date

### Included Data Challenges

- Duplicate SKU IDs
- Negative Stock Values
- Blank Supplier Names
- Inconsistent Category Names
- Missing Reorder Levels

---

## 📂 Project Files

### 📁 Dashboard File
[Download Dashboard](YOUR_EXCEL_DASHBOARD_LINK_HERE)

### 📁 Dataset File
[Download Dataset](YOUR_DATASET_LINK_HERE)

---

## 🎯 Business Value

This dashboard enables organizations to:

- Monitor inventory levels efficiently
- Identify products requiring replenishment
- Optimize warehouse inventory management
- Analyze supplier dependencies
- Improve operational decision-making
- Support inventory planning and control

---

## 📌 Key Insights

- Identified low stock products requiring immediate attention.
- Analyzed inventory distribution across warehouses.
- Evaluated supplier contribution to inventory.
- Monitored monthly stock movement trends.
- Delivered actionable inventory insights through interactive reporting.

---

## 🚀 Future Enhancements

- Inventory Forecasting
- ABC Inventory Analysis
- Safety Stock Calculation
- Supplier Lead Time Analysis
- Automated Inventory Reporting
