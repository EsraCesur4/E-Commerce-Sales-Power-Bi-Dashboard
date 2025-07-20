# 🛒 E-Commerce Sales and Customer Analysis – Power BI Dashboard

This Power BI project analyzes a large-scale e-commerce dataset to explore general sales metrics, customer profiles, and product category trends. The dashboard enables interactive filtering and insightful visualizations for both business overviews and detailed customer behavior analysis.

---

## Project Overview

This dashboard uses e-commerce data integrated from multiple tables (Users, Orders, Order Details, Products, Addresses, Regions) to uncover insights about:

- Total sales and revenue performance
- Customer-based metrics (unique users, average revenue per customer, order behavior)
- Temporal patterns (hour-based and weekday vs weekend sales)
- Regional and demographic customer distribution
- Product category preferences by age group and location

---

## Dashboard Preview

🔗 [View the Full Power BI Dashboard](https://app.powerbi.com/reportEmbed?reportId=6b491ab9-e2fb-429c-94eb-5d7b9aa97889)

| Start Page | Sales & Customer Overview | Customer Insights | Category Insights |
|------------|----------------------------|-------------------|-------------------|
| ![Start](Dashboard%20Pages/Start_Page.png) | ![Overview](Dashboard%20Pages/General_Overview_Page.png) | ![Customer](Dashboard%20Pages/Customer_Perspective_Page.png) | ![Category](Dashboard%20Pages/Product_Category_Perspective_Page.png) |

---

## Dashboard Structure

The report contains **3 main analysis pages** and a **Start Page** for navigation:

### 📄 Start Page
- Introduction to the project and its goals
- Page descriptions and navigation buttons

### 📄 Page 1 – Sales and Customer Overview
This page provides a general summary of total performance metrics and sales trends.

**Visuals Included:**
- KPI Cards:  
  - Total Sales Quantity (2.92M)  
  - Total Revenue (132B TL)  
  - Unique Customers (101K)  
  - Avg. Orders and Revenue per Customer  
  - Avg. Order Value (792K TL)  
  - Total Order Count
- Hourly Sales by Revenue (Line Chart)
- Regional Sales Map and Bar Chart (by city/region)
- Weekday vs Weekend Sales Pie Chart

### 📄 Page 2 – Customer Perspective
This section dives into demographic distribution and purchasing behavior.

**Visuals Included:**
- Gender Distribution (Pie Chart)
- Age Group Sales Comparison (Bar Chart)
- Gender & Region Cross Distribution (Stacked Bar Chart)
- Top 10 Customers in Istanbul (Table)
- Customer Count by Region (Pie Chart)

### 📄 Page 3 – Category Perspective
This page focuses on **category-level trends**, especially for young consumers in Istanbul.

**Visuals Included:**
- Treemap of Total Revenue by Product Category  
  (Filtered by age group 0–20 and city = Istanbul)

---

## DAX Highlights

Several calculated columns and measures were created using DAX to enrich analysis:

| Table           | DAX Column/Measure     | Description |
|------------------|-------------------------|-------------|
| `SiparisDetay`   | `ToplamSatisAdeti`      | SUM of `amount` |
| `Siparis`        | `ToplamCiro`            | SUM of `totalprice` |
| `Siparis`        | `ToplamMusteri`         | COUNT of distinct `UserID` |
| `SiparisDetay`   | `OrtalamaSiparisTutari` | AVERAGE of `linetotal` |
| Custom Measure   | `MusteriBasiCiro`       | `ToplamCiro` / `ToplamMusteri` |
| Custom Measure   | `MusteriBasiAdet`       | `ToplamSatisAdeti` / `ToplamMusteri` |

---

## Filters (Slicers) Used

All pages include interactive slicers for:

- Age Group (`YasGrubu`)
- Gender (`Gender`)
- Region (`BolgeAd`)
- Product Category (`YENIANAKATEGORI`)

These filters are synced across all report pages for dynamic exploration.

---

## 🗃️ File Structure  
📁 E-Commerce-Sales-Power-Bi-Dashboard 
├── 📁 Dashboard Pages  
│   ├── Start_Page.png  
│   ├── General_Overview_Page.png  
│   ├── Customer_Perspective_Page.png  
│   └── Product_Category_Perspective_Page.png  
├── 📁 Dataset Tables  
│   ├── SehirlerBolgeler.xlsx  
│   ├── adres.csv  
│   ├── items.csv  
│   ├── orderdetail.csv  
│   ├── orders.csv  
│   └── users.csv  
├── 📁 Power Bi  
│   └── E_Ticaret_Satış_Analizi_Power_Bi.pbix  
└── README.md  


