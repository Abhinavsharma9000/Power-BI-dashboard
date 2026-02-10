#### 📊 Blinkit Sales Dashboard – Power BI Project

An interactive and real-time **Power BI dashboard** built to analyze and visualize sales data for **Blinkit**, a leading grocery delivery platform. This project enables stakeholders to monitor key performance indicators, identify trends, and make faster data-driven decisions using a visually compelling dashboard.

---

## 🧾 Project Overview

The primary goal of this project is to present Blinkit's sales performance in an interactive dashboard, allowing real-time monitoring of:

- **Revenue generation**
- **Top-selling products**
- **Regional performance trends**
- **Sales breakdown by category and customer type**

The dashboard leverages dynamic filtering and DAX measures to help business users easily slice and drill down into sales metrics for operational and strategic decisions.

---

## 🎯 Objectives

- Create a centralized and visual representation of Blinkit’s sales data.
- Enable category, region, and time-based drilldowns.
- Improve sales insight turnaround time using automated data refresh.

---

## 📁 Features

### 🔹 Dashboard Highlights

- **Key KPIs:** Total Sales, Orders, Quantity Sold, Revenue by Region
- **Top N Products:** Visuals showing top-selling items
- **Geographic Heatmap:** Sales performance by zone/region
- **Dynamic Filtering:** Filter by product category, customer type, and sales channel
- **Time Intelligence:** Year-month slicers, time comparison using DAX

### 🧠 DAX Measures Used

- `Total Sales = SUM(Sales[TotalAmount])`
- `Average Order Value = [Total Sales] / DISTINCTCOUNT(Sales[OrderID])`
- `Top Products by Revenue = RANKX(ALL(Products[ProductName]), [Total Sales], , DESC)`
- Date intelligence (e.g., YTD, MOM comparisons) using `DATESYTD`, `SAMEPERIODLASTYEAR`

### ⚙️ Automation & Refresh

- Scheduled data refresh set up for seamless updates.
- Parameterized queries for flexible data load.

---

## 🛠️ Tools & Technologies

- **Power BI Desktop**
- **DAX (Data Analysis Expressions)**
- **Power Query (M Language)**
- **Excel (Data Source)**
- **Data Modeling (Star Schema)**

---

## 🧩 Data Model Design

This project follows a **star schema** approach, with:

- **Fact Table:** Sales Data (OrderID, Date, Quantity, Unit Price, Total Sales)
- **Dimension Tables:** 
  - `dimDate` – Order Date breakdown
  - `dimProduct` – Product categories
  - `dimRegion` – Geographic segmentation
  - `dimCustomer` – Customer type (e.g., new vs returning)

---

## 📌 Use Cases

- Real-time sales monitoring for Blinkit executives and category managers
- Identifying top revenue-generating products and regions
- Supporting pricing and stock decisions based on historical trends

---

## 📸 Dashboard Preview

*(Include screenshot here if available)*  
![Dashboard Preview](./dashboard-preview.png)

---

## 🔗 How to Use

1. Download the `.pbix` file from this repo.
2. Open in Power BI Desktop.
3. Connect to your own Excel or SQL data (optional).
4. Customize filters or visuals as needed.
5. Publish to Power BI Service for scheduled refresh & sharing.
