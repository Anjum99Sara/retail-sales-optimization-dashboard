# Retail Sales Optimization Dashboard

A two-page interactive business intelligence dashboard built to surface delivery inefficiencies, return rate patterns, and profitability drivers across customer segments, product categories, and geographies.

---

## Table of Contents
- <a href="#business-problem">Business Problem</a>
- <a href="#dashboard-overview">Dashboard Overview</a>
- <a href="#technical-stack">Technical Stack</a>
- <a href="#dashboard-structure">Dashboard Structure</a>
- <a href="#business-recommendations-from-analysis">Business Recommendations</a>
- <a href="#how-to-use">How to Use</a>
- <a href="#dataset">Dataset</a>
- <a href="#author">Author</a>

---

## Business Problem

Retail operations generate high volumes of transactional data, but without structured analysis, critical signals  late deliveries, high-return ship modes, underperforming segments remain invisible to decision-makers.

This dashboard answers three operational questions directly:

1. **Where is delivery performance breaking down?**  across segments, categories, and ship modes
2. **Which ship modes and salespeople are driving return rates?**  and is that correlated with order volume?
3. **Which products, segments, and customers are generating the most profit?**  and where is revenue being lost?

---

## Dashboard Overview

### Page 1 — Delivery & Return Rate

| Metric | Value |
|---|---|
| Total Customers | 793 |
| Total Orders | 5,000 |
| Average Delivery Days | 34.61 |
| Return Rate | 5.9% |

**Key findings:**

- Average delivery sits at **34.61 days**  far outside standard industry benchmarks (1–10 business days for most ship modes), indicating a significant gap between customer expectations and operational reality
- **Standard Class** accounts for the highest order volume (2,994 orders) but also the most deliveries exceeding 10 business days (918), making it the primary driver of late fulfillment
- **Same Day** shipping carries the highest return rate at **7.2%**, while Standard Class has the lowest at **5.6%** — counterintuitive and worth investigating: faster delivery may be creating mismatched expectations
- **Technology** has the slowest average delivery at **35.08 days** vs Furniture at **34.37 days**  a small but consistent gap worth monitoring given Technology's higher profit margins
- Top-performing salesperson (lowest return rate): **Cassandra Brandow at 2.9%**; highest: **Anna Andreadi at 11.7%** — a 4× spread that warrants further review of customer handling or product mix

---

### Page 2 — Profitability & Efficiency

| Metric | Value |
|---|---|
| Total Sales | $733.22K |
| Total Quantity | 12K units |
| Total Profit | $147.28K |
| Revenue Lost | -$53.84K |

**Key findings:**

- **Technology** generates the most profit ($63K) despite lower unit volume — highest margin category
- **Furniture** lags significantly ($22K profit) relative to its operational complexity and delivery cost
- **Consumer segment** drives the most profit ($68K), more than Corporate and Home Office combined
- Sales are **down 2.1% vs prior month** but **up 20.4% vs prior year**  short-term dip within a strong growth trajectory
- Revenue lost figure of **-$53.84K** represents discounts, returns, and write-offs; at 7.3% of gross sales, this is a material leakage worth targeting

---

## Technical Stack

| Tool | Purpose |
|---|---|
| Power BI | Dashboard development, DAX measures, interactive filtering |
| DAX | KPI calculations, period-over-period comparisons (vs PM, vs PY), efficiency metrics |
| Data Modeling | Star schema with fact/dimension tables for orders, customers, products, geography |

---

## Dashboard Structure

```
retail-sales-dashboard/
│
├── RetailSalesOptimizationDashboard.pbix     # Main Power BI file
├── data/
│   └── retail_orders.xlsx         # Source dataset
├── screenshots/
│   ├── page1_delivery_and_returns_rate.png
│   └── page2_profitability_efficiency.png
└── README.md
```

---

## Business Recommendations (from analysis)

1. **Audit Same Day shipping returns**  highest return rate at 7.2% despite being the fastest ship mode. Investigate whether product condition, incorrect orders, or expectation mismatch is the driver.

2. **Review Anna Andreadi's customer portfolio**  11.7% return rate is an outlier. Either she handles the highest-risk accounts or there's a process issue worth addressing.

3. **Prioritize Furniture margin improvement**  lowest profit ($22K) among three categories with comparable operational overhead to Office Supplies ($61K). Either renegotiate supplier costs or reduce discounting.

4. **Target the -$53.84K revenue leakage**  at 7.3% of gross sales, reducing discounts and return-driven write-offs by even 30% recovers ~$16K annually with no additional revenue required.

5. **Investigate delivery delay root cause**  34+ day average across all ship modes suggests fulfillment or warehouse bottleneck, not just carrier delays. Standard Class with 918 orders >10 days is the priority queue.

---

## How to Use

1. Open `RetailSalesOptimizationDashboard.pbix` in Power BI Desktop
2. Use the **Segment**, **Year**, **Category**, and **State/City** slicers to filter all visuals
3. Toggle between **Delivery and Return Rate** and **Profitability and Efficiency** pages using the top-right buttons
4. Hover over charts for detailed tooltips

---

## Dataset

- **Records:** ~10,000 order rows
- **Fields include:** Order ID, Customer Name, Segment, Region, Category, Sub-Category, Sales, Quantity, Discount, Profit, Ship Mode, Ship Date, Order Date

---

## Author

**[Sara Anjum]**
Data Analyst | Power BI | Business Intelligence

[LinkedIn](https://www.linkedin.com/in/sara-anjum2000/) · [Email](mailto:anjumsara8276@gmail.com)

---
