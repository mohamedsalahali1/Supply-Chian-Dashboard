# 📊 Supply Chain Analytics Dashboard

---

## 📌 Overview
This project presents an end-to-end Supply Chain Analytics Dashboard built using Power BI.  
It provides a comprehensive analysis of business operations across Sales, Inventory, Production, Procurement, and Shipment.

The goal is to transform raw data into actionable insights that support data-driven decision-making and improve overall operational efficiency.

---

## 🎯 Objectives
- Monitor overall business performance  
- Identify inefficiencies across supply chain operations  
- Optimize inventory and procurement decisions  
- Improve delivery performance  
- Analyze sales and profitability  

---

## 📊 Dataset Description

The dataset follows a **Star Schema** design:

### 🔹 Dimension Tables
- dim_customer → customer details (location, segment, size)  
- dim_product → product information (category, cost, price)  
- dim_date → time-based analysis (year, month, day)  
- dim_supplier → supplier performance and quality  
- dim_facility → production facilities  

### 🔸 Fact Tables
- fact_sales → revenue, profit, discounts  
- fact_inventory → stock levels, safety stock, reorder point  
- fact_production → production output, defects  
- fact_shipment → delivery performance, shipping cost  
- procurement → supplier orders, cost, lead time  

---

## 🔗 Data Model
- Star Schema structure  
- One-to-Many relationships 

- Central fact tables connected to dimensions
- 
 <img width="1221" height="701" alt="Multi Star Schema" src="https://github.com/user-attachments/assets/d9c25c20-a424-4596-8967-ec350fad0a83" />

---

## 🛠 Tools Used
- Power BI  
- DAX (Data Analysis Expressions)  
- Data Modeling  
- Data Cleaning  

---

## 🧠 Key DAX Measures

### 🔹 Production Efficiency
```DAX
Production Efficiency =
DIVIDE(
    [Total Units Produced] - [Defective units],
    [Total Units Produced]
)
```

### 🔹 Stock Coverage Days
```DAX
Stock Coverage Days =
DIVIDE(
    SUM(fact_inventory[stock_level]),
    SUM(fact_sales[quantity_sold])
) * 30
```

### 🔹 Stock Status
```DAX
Stock Status =
SWITCH(
    TRUE(),
    [Current Stock Level] < [Reorder point], "Critical",
    [Current Stock Level] < [Safety Stock], "Low",
    "Good"
)
```

---

# 📊 Dashboard Pages

---

## 🟦 Executive Dashboard

<img width="1416" height="845" alt="executive" src="https://github.com/user-attachments/assets/12348bab-5514-4401-85c6-bc1e20fcfc14" />

### 📌 KPIs
- Total Revenue → $176.95M  
- Total Profit → $48.56M  
- Profit Margin → 27.44%  
- Total Orders → 8,499  
- Cash Cycle Days → 25.72  
- Perfect Order Rate → 75.29%  

### 📊 Key Insights
- Samsung Vietnam & Samsung India have the best lead time (9 days)  
- Amazon is the top revenue contributor (~37M)  
- Profit contribution is consistent across major customers  
- USA has the highest shipping cost  

### 🎯 Purpose
Provides a high-level overview of overall business performance and supports strategic decision-making.

---

## 🏭 Supplier 

<img width="1415" height="848" alt="Supplier page" src="https://github.com/user-attachments/assets/5d9822f6-7af4-4668-bcc7-301d358f5d60" />


### 📌 KPIs
- Total Procurement Cost → 78M  
- Avg Lead Time → 11.53 days  
- Supplier Quality → 94%  
- Order Fulfillment → 94%  

### 📊 Key Insights
- Procurement cost peaks in October and December (seasonality effect)  
- Smartphones category drives the highest revenue and profit  
- Suppliers with lower lead time significantly improve operational efficiency  

### 🎯 Purpose
Evaluate supplier performance and optimize procurement strategy.

---

## 🏗 Production Analysis

<img width="1415" height="848" alt="Supplier page" src="https://github.com/user-attachments/assets/d0465cfd-408c-4130-8f1e-5c7b595ba756" />
### 📌 KPIs
- Total Units Produced → 4M units  
- Defective Units → 24K  
- Defect Rate → 0.63%  
- Production Efficiency → 99.37%  
- Daily Production → 5.24K units  

### 📊 Key Insights
- Production peaked in October (411K) and December (398K)  
- Highest growth observed in October (+167% MoM)  
- Galaxy S24 Ultra & Watch6 Classic are top-performing products  
- Overall production quality is very high (low defect rate)  

### 🎯 Purpose
Monitor production efficiency, output trends, and product quality.

---
## 📦 Inventory Analysis

<img width="1416" height="842" alt="inventory page" src="https://github.com/user-attachments/assets/926582b9-3ffb-4d52-82d5-8c91c562ff19" />

### 📌 KPIs
- Inventory Value → 108.77M  
- Stock Coverage → 25.63 days  
- Inventory Accuracy → 86.9%  
- Inventory Turnover → High  
- Stock Status → Good  

### 📊 Key Insights
- Strong inventory turnover indicates high product movement  
- Current stock levels are sufficient to support sales demand  
- Inventory is well-balanced with minimal overstock risk  

### 🎯 Purpose
Manage stock levels efficiently and ensure availability without excess inventory.

---

## 🚚 Shipment Analysis

<img width="1412" height="846" alt="shipment page" src="https://github.com/user-attachments/assets/a557a4bb-3e3a-46ae-9b2e-72609a5b04ea" />


### 📌 KPIs
- Total Shipments  
- On-Time Delivery %  
- Shipping Cost  

### 📊 Key Insights
- Shipping cost is highest in USA region  
- Delivery performance varies across carriers  
- Some shipments experience delays due to operational inefficiencies  

### 🎯 Purpose
Improve logistics efficiency and optimize delivery performance.

---

## 💰 Sales Analysis

<img width="1282" height="771" alt="sales page" src="https://github.com/user-attachments/assets/bc90d5d9-e5b7-40b8-a081-88fe572035c4" />

### 📌 KPIs
- Total Revenue  
- Total Profit  
- Profit Margin  
- AOV (Average Order Value)  

### 📊 Key Insights
- Smartphones generate the highest revenue and profit  
- Discounts impact profitability across some products  
- Revenue growth varies across customers and time periods  

### 🎯 Purpose
Analyze customer behavior, sales performance, and profitability.

---

## 🔍 Key Insights Summary
- Strong seasonal patterns in procurement and production (October & December)  
- High-performing suppliers improve operational speed  
- Inventory turnover reflects strong demand  
- Shipping cost optimization is required  
- Discounts impact overall profitability  

---

## 💡 Recommendations
- Focus on suppliers with lower lead time  
- Optimize shipping strategies to reduce costs  
- Prepare for seasonal demand spikes  
- Improve inventory planning and monitoring  
- Optimize pricing and discount strategies  

---

## 📌 Conclusion
This dashboard demonstrates how data analytics can transform complex supply chain data into meaningful insights, enabling businesses to monitor performance, identify issues, and make informed decisions.
