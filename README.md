# olist-ecommerce-powerbi-dashboard
# 📊 E-Commerce Sales & Logistics Analytics Dashboard (Olist Dataset)

An end-to-end Power BI analytics solution exploring sales performance, logistics operations, and customer satisfaction metrics using Brazilian e-commerce data.

---

## 📌 Project Overview
This project provides an executive-level interactive dashboard designed to help stakeholders monitor revenue trends, optimize supply chain efficiency, and identify factors affecting customer satisfaction.

The dashboard consists of 3 main views:
1. **Sales Performance:** High-level executive KPIs, regional sales distribution, and category performance.
2. **Logistics Overview:** Supply chain efficiency, shipping costs, order cycle times, and review score correlations.
3. **Insights & Recommendations:** Data-driven strategic takeaways to optimize business growth and operational fulfillment.

---

## 📷 Dashboard Preview

### 1. Sales Performance Dashboard
![Sales Performance](docs/sales_performance.png)

### 2. Logistics Overview
![Logistics Overview](docs/logistics_overview.png)

### 3. Executive Insights & Recommendations
![Insights & Recommendations](docs/executive_insights.png)

---

## 🔑 Key Business Insights

* **Sales & Revenue Drivers:** Total revenue reached **$13M** across **96K orders**, heavily driven by **Beleza Saude ($1.23M)** and top geographic markets like **Sao Paulo (120.43K orders)**.
* **Seasonality Trends:** Strong seasonal surge in **July–August ($1.81M)** compared to lower performance in **January ($0.71M)**.
* **Logistics & Customer Impact:** Overall review score is **4.09**, but ratings drop significantly below **2 stars** when the order cycle time exceeds **40 days**.
* **Delivery Bottlenecks:** Fulfillment speed fluctuates, achieving its best performance in **August (9.12 days)** and worst delays in **March (15.65 days)**.

---

## 💡 Strategic Recommendations

1. **Targeted Expansion:** Focus marketing spend on top revenue hubs (**Sao Paulo & Rio de Janeiro**) and high-value categories (**Beleza Saude**).
2. **Seasonal Inventory Management:** Increase inventory and logistics capacity ahead of peak demand in **July–August**.
3. **Strict Fulfillment SLA:** Enforce a maximum **20-day delivery threshold** across all regions to preserve customer review scores above **4 stars**.
4. **Q1 Operational Optimization:** Address supply chain bottlenecks in **Q1 (Jan–Mar)** to reduce overall delivery delays.

---

## 🛠️ Data Model & DAX Measures
- **Data Model:** Star Schema with a centralized `Fact_Orders` table connected to dimensional tables (`Dim_Customers`, `Dim_Products`, `Dim_Sellers`, `Dim_Calendar`).
- **Key Dax Formulas:**
  - `Total Revenue = SUM(Sales[Price])`
  - `AOV = DIVIDE([Total Revenue], [Total Orders])`
  - `Avg Delivery Days = AVERAGE(Sales[Order Cycle Time])`

---

## 📂 Project Structure
```text
├── data/                  # Cleaned dataset / CSV files
├── docs/                  # Dashboard screenshots for README
├── Olist_Analytics.pbix   # Main Power BI project file
└── README.md              # Project documentation
