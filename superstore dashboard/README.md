<div align="center">

# 📊 Superstore Sales Dashboard
### *An Interactive Power BI Dashboard for Sales, Profit, Quantity & Discount Analysis*

[![Power BI](https://img.shields.io/badge/Microsoft-Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![Pages](https://img.shields.io/badge/Report%20Pages-2-2E7D32?style=for-the-badge&logo=powerbi&logoColor=white)](https://powerbi.microsoft.com/)
[![Visuals](https://img.shields.io/badge/Visuals-KPI%20%7C%20BAR%20%7C%20SLICER%20%7C%20TABLE-FF6F00?style=for-the-badge&logo=powerbi&logoColor=white)](https://powerbi.microsoft.com/)
[![Dataset](https://img.shields.io/badge/Dataset-Sample%20Superstore-9C27B0?style=for-the-badge&logo=powerbi&logoColor=white)](https://powerbi.microsoft.com/)

<br/>

> *"Numbers sit quietly in a table — a dashboard makes them speak."*

</div>

---

## 📋 Table of Contents

- [📌 Overview](#-overview)
- [🎯 Problem Statement](#-problem-statement)
- [✨ Key Features](#-key-features)
- [🏗️ Project Structure](#️-project-structure)
- [🔄 Dashboard Workflow](#-dashboard-workflow)
- [🧾 Page-by-Page Explanation](#-page-by-page-explanation)
- [🖥️ Dashboard Screenshot](#️-dashboard-screenshot)
- [🛠️ Tech Stack](#️-tech-stack)
- [📈 Results & Insights](#-results--insights)
- [⚠️ Known Issues](#️-known-issues)
- [🏆 Advantages](#-advantages)
- [📄 License](#-license)
- [👤 Author](#-author)
- [🙏 Acknowledgements](#-acknowledgements)
- [🎥 Explanation Video](#-explanation-video)

---

## 📌 Overview

**Superstore Sales Dashboard** is a Power BI project that turns the well-known *Sample – Superstore* retail dataset into a clean, interactive one-page dashboard. It answers the everyday questions a store manager asks: *How much did we sell? How much profit did we make? Which region and which product category perform best?*

The report has **two pages**:

- **DashBoard** — four KPI cards, two slicers, and three bar charts for a quick business summary
- **Order Details** — a detailed order-level table with a navigation button, for checking the numbers behind the charts

This project is designed to:
- Summarise total **Sales, Profit, Quantity and Average Discount** in four KPI cards
- Compare **profit across regions** (West, East, South, Central)
- Compare **revenue across product categories** (Technology, Furniture, Office Supplies)
- Rank the **Top 5 sub-categories by sales**
- Let users **filter every visual** by Region and Category using slicers
- Provide an **order-level drill-down table** for detailed inspection

---

## 🎯 Problem Statement

> **Objective:** Build a single Power BI dashboard that gives management an instant, filterable view of sales performance — what sells, where it is profitable, and which products lead — without opening the raw data.

| 📂 Category | 🧩 Visual | 🔍 Description |
|-------------|-----------|----------------|
| KPI Summary | 4 Cards | Total Sales, Total Profit, Total Quantity, Average Discount |
| Filtering | 2 Slicers | Select Region and Select Category (dropdown style) |
| Regional Analysis | Bar Chart | Total Profit by Region |
| Category Analysis | Bar Chart | Total Revenue by Product Category |
| Product Analysis | Bar Chart | Top 5 Sub-Categories by Sales |
| Detail View | Table | Order ID, date, customer, region, category, sub-category and measures |

---

## ✨ Key Features

| Feature | Description |
|--------|-------------|
| 🔢 **KPI Cards** | Four headline numbers: **1.5M** sales, **178.57K** profit, **24,936** units, **15.70%** average discount |
| 🎛️ **Dropdown Slicers** | *Select Region* and *Select Category* filter all visuals at once |
| 📊 **Profit by Region** | Horizontal bars ranked West → East → South → Central |
| 🟥 **Revenue by Category** | Technology, Furniture and Office Supplies compared side by side |
| 🏅 **Top 5 Sub-Categories** | Chairs, Phones, Storage, Tables and Binders ranked by sales |
| 💬 **Tooltips** | Hover over any bar to see the chart name and exact value |
| 📄 **Order Details Page** | Table of individual orders with a button to move between pages |
| 🎨 **Clean Layout** | Bold blue title, light-grey canvas, and consistent colour per chart |

---

## 🏗️ Project Structure

```
📦 superstore-sales-dashboard/
│
├── 📄 Superstore_Dashboard.pbix   ← Main Power BI report (entry point)
│
├── 🖼️ images/
│   └── dashboard.png              ← Screenshot of the dashboard
│
└── 📄 README.md                   ← Project documentation
```

**Pages inside `Superstore_Dashboard.pbix`:**

```
📄 Page 1 : DashBoard        ← KPI cards, slicers and 3 bar charts
📄 Page 2 : Order Details    ← Order-level table with navigation button
```

**Data table used:** `Sample - Superstore`

| Field | Used For |
|-------|----------|
| `Order ID`, `Order Date` | Identifying each order and when it happened |
| `Customer Full Name` | Who placed the order |
| `Region` | Slicer and *Total Profit by Region* chart |
| `Category` | Slicer and *Total Revenue by Product Category* chart |
| `Sub Category` | *Top 5 Sub-Categories by Sales* chart |
| `Sales`, `Profit`, `Quantity`, `Discount` | KPI cards, chart values and table measures |

---

## 🔄 Dashboard Workflow

```
Load Sample - Superstore Data
      │
      ▼
┌──────────────────────────────┐
│   Data Model                 │  ← Single table: orders, customers, measures
└─────────────┬────────────────┘
              │
              ▼
┌──────────────────────────────┐
│   KPI Cards                  │  ← Sum of Sales / Profit / Quantity, Avg Discount
└─────────────┬────────────────┘
              │
              ▼
┌──────────────────────────────┐
│   Slicers                    │  ← Region and Category filters
└─────────────┬────────────────┘
              │
              ▼
┌──────────────────────────────┐
│   Bar Charts                 │  ← Profit by Region, Revenue by Category, Top 5 Sub-Categories
└─────────────┬────────────────┘
              │
              ▼
┌──────────────────────────────┐
│   Order Details Page         │  ← Row-level table for verification
└─────────────┬────────────────┘
              │
              ▼
     Insights Ready ✅
```

---

## 🧾 Page-by-Page Explanation

### 🏠 Page 1 — `DashBoard`

#### 🔢 KPI Cards

| Card | Value | Meaning |
|------|-------|---------|
| **Sum of Sales** | 1.5M | Total revenue across all orders |
| **Sum of Profit** | 178.57K | Total profit earned |
| **Sum of Quantity** | 24,936 | Total units sold |
| **Average of Discount** | 15.70% | Average discount given per order line |

#### 🎛️ Slicers

| Slicer | Field | Purpose |
|--------|-------|---------|
| **Select Region** | `Region` | Show data for one or more regions (default: *All*) |
| **Select Category** | `Category` | Show data for one or more categories (default: *All*) |

#### 📊 Charts

| Chart | Axis | Value | Insight |
|-------|------|-------|---------|
| **Total Profit by Region** | `Region` | Sum of `Profit` | Shows which region earns the most profit |
| **Total Revenue by Product Category** | `Category` | Sum of `Sales` | Shows which category brings the most revenue |
| **Top 5 Sub-Categories by Sales** | `Sub Category` | Sum of `Sales` | Shows the best-selling product groups |

---

### 📄 Page 2 — `Order Details`

A table that lists each order with these columns:

```
Order ID | Order Date | Customer Full Name | Region | Category | Sub Category
Sales | Profit | Quantity | Discount
```

A button on this page lets the user move between the dashboard and the detailed table, so any chart value can be cross-checked against the raw orders.

---

## 🖥️ Dashboard Screenshot

<div align="center">

![Superstore Sales Dashboard]("<img width="1307" height="737" alt="dashboard" src="https://github.com/user-attachments/assets/7f42c2ef-ee09-41cc-b509-d63c839e5ee0" />
")

*Superstore Sales Dashboard — KPI cards, slicers, and bar charts in Power BI Desktop*

</div>

```
Sample Output — Total Profit by Region
+----------+-----------+
| Region   |    Profit |
+----------+-----------+
| West     |    65.70K |
| East     |    50.11K |
| South    |    37.59K |
| Central  |    25.17K |
+----------+-----------+

Sample Output — Total Revenue by Product Category
+------------------+----------+
| Category         |    Sales |
+------------------+----------+
| Technology       |  503.0K  |
| Furniture        |  502.2K  |
| Office Supplies  |  491.6K  |
+------------------+----------+
```

---

## 🛠️ Tech Stack

| Tool | Version | Purpose |
|------|---------|---------|
| 📊 **Microsoft Power BI Desktop** | Latest | Building the report and dashboard |
| 🗃️ **Sample – Superstore Dataset** | Excel / CSV | Source data for orders, sales and profit |
| 🔧 **Power Query** | Built-in | Loading and shaping the data |
| 📐 **Aggregations** | Built-in | Sum of Sales, Profit, Quantity; Average of Discount |
| 🎛️ **Visuals** | Built-in | Card, Clustered Bar Chart, Slicer, Table, Button |

---

## 📈 Results & Insights

After opening the dashboard, the following insights are visible:

- 💰 **Overall Performance** — Sales of about **1.5M** produced a profit of **178.57K**, roughly a **12% profit margin**
- 🌍 **Best Region** — **West** leads with **65.7K** profit; **Central** is lowest with **25.17K**
- 📦 **Category Balance** — **Technology (503.0K)** and **Furniture (502.2K)** are almost tied, with **Office Supplies (491.6K)** close behind
- 🪑 **Top Sub-Category** — **Chairs** lead in sales, followed closely by **Phones**, then Storage, Tables and Binders
- 🏷️ **Discounting** — Orders carry an average discount of **15.70%**, a useful point to watch against profit
- 🛒 **Volume** — **24,936** units sold in total across the period shown (FY 2014–2017)

---

## ⚠️ Known Issues

| Issue | Detail |
|-------|--------|
| 📥 **Power BI Desktop needed** | The `.pbix` file opens only in Power BI Desktop (Windows) |
| 📊 **Top 5 chart labels** | The Top 5 Sub-Categories chart shows values only on the axis, not as data labels |
| 🗃️ **Static dataset** | The data is a fixed sample, so numbers do not refresh from a live source |
| 🔍 **Rounded KPIs** | Cards show shortened values (e.g. **1.5M**), so exact totals are visible only in the Order Details table |

---

## 🏆 Advantages

| Advantage | Detail |
|-----------|--------|
| 🎓 **Beginner Friendly** | Simple one-table model, easy to understand and recreate |
| 👀 **At-a-Glance Insights** | KPIs and charts fit on a single page |
| 🎛️ **Fully Interactive** | Slicers update all visuals instantly |
| 🔎 **Traceable Numbers** | Order Details page lets every chart be verified |
| 🧪 **Extensible** | Easy to add Segment, State, Ship Mode, or a Year-wise trend line |
| 📖 **Readable Design** | Clear titles, consistent colours, and a clean layout |

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for full details.

```
MIT License — Free to use, modify, and distribute with attribution.
```

---

## 👤 Author

<div align="center">

### Priya Vadsak

[![GitHub](https://img.shields.io/badge/GitHub-23se02ml213--design-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/23se02ml213-design)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/priya-vadsak-4347294300/)

> *"Every great dashboard starts with a good question — and ends with a clear answer."*

**🎓 Role:** Power BI Learner \
**📍 Location:** India \
**🛠️ Skills:** Power BI, Data Analysis, Python

</div>

---

## 🙏 Acknowledgements

Special thanks to the following resources and communities that made this project possible:

- 📚 [Microsoft Power BI Documentation](https://learn.microsoft.com/power-bi/) — Official reference for visuals and reports
- 🗃️ Sample – Superstore Dataset — Widely used retail dataset for learning BI
- 🔍 [W3Schools](https://www.w3schools.com/) — Beginner reference
- 🧠 [GeeksForGeeks](https://www.geeksforgeeks.org/) — Concept explanations
- 💬 [Stack Overflow Community](https://stackoverflow.com/) — Problem-solving support

---

## 🎥 Explanation Video

A complete walkthrough of this dashboard — data, visuals, slicers and insights — is available here:

[![Watch on Google Drive](https://img.shields.io/badge/▶%20Watch-Explanation%20Video-4285F4?style=for-the-badge&logo=googledrive&logoColor=white)](https://drive.google.com/drive/folders/11ow--aWfh9l2kbS6oP8Kj8S7JGJrUED1)

🔗 **Link:** https://drive.google.com/drive/folders/11ow--aWfh9l2kbS6oP8Kj8S7JGJrUED1

---

<div align="center">

*Made with ❤️ and ☕ — Last updated: October 2026*

</div>
