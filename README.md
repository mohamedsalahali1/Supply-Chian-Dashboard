SAMSUNG
Supply Chain Analytics Dashboard
─────────────────────────────
Project Documentation & Insights Report
Power BI  •  DAX  •  Data Modeling

📌 Overview

This project is an end-to-end Supply Chain Analytics Dashboard built using Power BI. It analyzes key business operations including Sales, Inventory, Production, Procurement, and Shipment to provide actionable insights and support data-driven decision-making.

🎯 Objectives

•	Monitor overall business performance
•	Identify inefficiencies in supply chain operations
•	Optimize inventory and procurement decisions
•	Improve delivery performance
•	Analyze sales and profitability





📊 Dataset

The dataset follows a star schema and includes:

Dimension Tables
•	dim_customer
•	dim_product
•	dim_date
•	dim_supplier
•	dim_facility

Fact Tables
•	fact_sales
•	fact_inventory
•	fact_production
•	fact_shipment
•	procurement














🔗 Data Model

•	Star Schema design
•	One-to-Many relationships
•	Fact tables connected to dimension tables

 

🛠 Tools Used

📊 Power BI
Dashboard & Visualization	🧠 DAX
Measures & Calculations
🔗 Data Modeling
Star Schema	🧹 Data Cleaning
Transformation & Prep

🧠 Key DAX Measures


Production Efficiency
Production Efficiency =
DIVIDE(
    [Total Units Produced] - [Defective units],
    [Total Units Produced]
)

Stock Coverage Days
Stock Coverage Days =
DIVIDE(
    SUM(fact_inventory[stock_level]),
    SUM(fact_sales[quantity_sold])
) * 30

Stock Status
Stock Status =
SWITCH(
    TRUE(),
    [Current Stock Level] < [Reorder point], "Critical",
    [Current Stock Level] < [Safety Stock], "Low",
    "Good"
)


📊 Dashboard Pages


📊 1. Executive Overview

💰 Total Revenue
176.95M	📈 Total Profit
48.56M
📉 Profit Margin
27.44%	🛒 Total Orders
8,499
⏱ Cash Cycle Days
25.72	✅ Perfect Order Rate
75.29%
💸 Cost Ratio %
72.56%	

💡 Key Insights
•	Samsung Vietnam & India have the best lead time (9 days)
•	Amazon.com is the top revenue contributor (~$37M)
•	USA has the highest shipping cost and delivery volume
•	All top platforms maintain a consistent ~$10M profit

🎯 Purpose: Provides a high-level overview of overall business performance across all supply chain functions.

 

🏭 2. Supplier & Procurement

💵 Procurement Cost
78.13M	📦 Total Order Qty
129K
💲 AVG Unit Cost
645.77	⏳ AVG Lead Time
11.53 days
⭐ Avg Supplier Quality
96.63%	🔄 Reorder Frequency
2,200
🏢 Number of Suppliers
7	

💡 Key Insights
•	October and December show peak procurement cost — seasonal demand spike
•	Smartphones category drives the highest revenue and profit
•	Galaxy S24 Ultra has the highest order quantity (16,990 units)
•	Procurement cost MoM peaked at 168.47% in October

🎯 Purpose: Evaluate supplier performance, procurement efficiency, and seasonal cost patterns.

 

🏗 3. Production Analysis

🏭 Total Units Produced
4M	⚠️ Defective Units
24K
📉 Avg Defect Rate
0.63%	⚙️ Production Efficiency
99.37%
📅 Production per Day
5.24K	

💡 Key Insights
•	Exceptionally high production efficiency at 99.37%
•	Peak production in October (411K) and December (398K)
•	Defect rate stays consistently low (0.59%–0.66% range)
•	Smartphones and tablets lead in quantity produced

🎯 Purpose: Monitor production performance, quality control, and output trends over time.

[ 📸 Production Overview — Dashboard Screenshot ]
← ضع صورة الصفحة هنا →

📦 4. Inventory Analysis

🔄 Inventory Turnover
924.99K	📅 Stock Coverage
25.63 days
💰 Inventory Value
108.77M	🎯 Inventory Accuracy
86.90%
✅ Stock Status
Good	

💡 Key Insights
•	Overall stock status is 'Good' — no critical shortages
•	Galaxy S24 leads in both inventory value and current stock level
•	Galaxy S24 Ultra shows heavy overstock vs other products
•	Current stock levels are consistently above reorder points

🎯 Purpose: Manage stock levels, detect overstock/understock situations, and optimize inventory health.

[ 📸 Inventory Overview — Dashboard Screenshot ]
← ضع صورة الصفحة هنا →

🚚 5. Shipment Analysis

📦 Total Shipments
7,500	✅ Delivered Shipments
5,647
🚛 In Transit
1,140	⚠️ Delayed Shipments
573
⏱ On-Time Delivery %
89.85%	💸 Total Shipping Cost
19.42M
📊 Total Qty Shipped
3M	

💡 Key Insights
•	On-time delivery rate is 89.85% — room for improvement
•	Carrier capacity is the leading delay reason
•	Amazon.com Inc. has the most delayed shipments (37)
•	Shipping costs peaked in December at 2.07M
•	In-transit shipments grew steadily through the year (82→116)

🎯 Purpose: Analyze logistics performance, identify delay causes, and optimize carrier selection.

[ 📸 Shipment Overview — Dashboard Screenshot ]
← ضع صورة الصفحة هنا →

💰 6. Sales Analysis

💰 Total Revenue
176.95M	📈 Total Profit
48.56M
📉 Profit Margin %
27.44%	🛒 Total Orders
8,499
💳 AVG Order Value
20.82K	✅ Perfect Order Rate
75.29%
💸 Cost Ratio %
72.56%	

💡 Key Insights
•	Amazon.com leads revenue at $36.75M (27.43% margin)
•	All top 5 platforms maintain ~27% profit margin
•	Galaxy S24 Ultra is the highest profit product (~$10M)
•	Sales peak in October–December (seasonal uplift)
•	Amazon and Samsung Direct Show YoY revenue growth (1.09x, 1.03x)

🎯 Purpose: Analyze sales performance, customer behavior, product profitability, and revenue trends.

[ 📸 Sales Overview — Dashboard Screenshot ]
← ضع صورة الصفحة هنا →

🔍 Key Insights

•	Seasonal peaks in procurement and production occur in October and December
•	Samsung Vietnam & India are top-performing suppliers with the shortest lead time (9 days)
•	Production efficiency is outstanding at 99.37% with minimal defect rate
•	Overall inventory health is Good with no critical stock shortages
•	On-time delivery is strong at 89.85% but carrier capacity causes most delays
•	Smartphones consistently generate the highest revenue and profit across all dimensions

💡 Recommendations

•	Prioritize Samsung Vietnam & India for procurement to reduce lead times
•	Investigate and address carrier capacity constraints to improve delivery rates
•	Prepare inventory buffer stock ahead of October–December seasonal spikes
•	Optimize shipping cost management — December peaks suggest need for carrier renegotiation
•	Continue leveraging Smartphone category strength while expanding Wearables segment

📌 Conclusion

This dashboard demonstrates how data analytics can transform raw supply chain data into actionable insights, enabling better decision-making across sales, operations, logistics, and procurement. The integrated Power BI model provides stakeholders with real-time visibility into KPIs, trends, and inefficiencies — driving continuous improvement across the entire Samsung supply chain.

🔗 Project Files

•	Power BI File (.pbix)
•	Dataset (Fact & Dimension Tables)
•	Dashboard Screenshots
•	This Documentation
