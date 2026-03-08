# Sales Performance Analysis – Retail & Corporate Sales Performance (2025)
> *An end-to-end analysis of multi-region sales data to identify revenue drivers, evaluate profitability, and recommend strategies for growth.*

---

## ⚙️ Project Type Flags

- [ ] Exploratory Data Analysis (EDA)
- [ ] Dashboard / Data Visualization
- [ ] Data Cleaning / Wrangling
- [ ] End-to-End

---

## Table of Contents
1. [Project Overview](#1-project-overview)
2. [Objectives](#2-objectives)
3. [Project Scope & Tools](#3-project-scope--tools)
4. [Repository Structure](#4-repository-structure)
5. [Data Workflow](#5-data-workflow)
6. [Data Model & Schema](#6-data-model--schema)
7. [Analysis & Metrics](#7-analysis--metrics)
8. [Key Insights](#8-key-insights)
9. [Recommendations](#9-recommendations)
10. [Assumptions & Limitations](#10-assumptions--limitations)
11. [Future Enhancements](#11-future-enhancements)
12. [Deliverables](#12-deliverables)
13. [Author](#13-author)

---

## 1. Project Overview

<!--
  Write 3–5 sentences in plain language.
  Cover: context → problem → approach → outcome.
  Read it out loud. If it sounds like a form - rewrite it.

  WHAT GOOD LOOKS LIKE:
  "A mid-size retail business was seeing inconsistent revenue across
  its regional stores but couldn't identify the root cause. This project
  explored 18 months of transaction data across five regions to determine
  whether underperformance was driven by sales volume, pricing, or return
  rates. The analysis revealed that one region's gap was almost entirely
  explained by an unusually high return rate on a single product category -
  a finding invisible in the company's top-level reporting."

  WHAT TO AVOID:
  "This project analyzes sales data to find trends and insights."
  (Too vague. Could describe 10,000 projects. Describes none of them.)
-->

**Context:** A retail company operating across four regions wanted to better understand its sales performance, revenue drivers, and profitability trends in 2025.

**Problem Statement:** Despite strong overall revenue, management lacked clear insights into which products, regions, and sales channels were contributing most to profitability.

**Approach:** Sales transaction data from January–May 2025 was cleaned, transformed, and analyzed using Excel and Power BI to evaluate regional performance, product profitability, customer segments, and sales channels.

**Outcome:** The analysis revealed key revenue drivers, identified the highest-performing products and regions, and produced actionable recommendations to improve profitability and support business expansion.

---

## 2. Objectives

<!--
  Write objectives that are specific enough to succeed or fail.
  Use action-oriented verbs: Identify, Determine, Quantify, Build, Evaluate.

  WHAT GOOD LOOKS LIKE:
  ✅ "Determine whether customer churn rate correlates with support ticket volume."
  ✅ "Identify the top three revenue-driving product categories across all regions."
  ✅ "Build a reproducible pipeline that ingests and cleans daily sales exports."

  WHAT TO AVOID:
  ❌ "Explore the data."
  ❌ "Gain insights."
  ❌ "Understand trends."
  (These can't fail - which means they can't succeed either.)
-->

- **Primary Objective:** Determine the key drivers of revenue and profit across regions, products, sales channels, and customer segments.
- **Secondary Objective 1:** Identify the top-performing products contributing most to profit.
- **Secondary Objective 2:** Evaluate regional sales performance across the four operating regions.
- **Secondary Objective 3:** Compare profitability across sales channels (Online vs In-Store).
- **Secondary Objective 3:** Assess differences in performance between Retail and Corporate customers.

> 💡 *Every analysis decision in this project traces back to one of these objectives.*

---

## 3. Project Scope & Tools

### Scope

<!--
  WHAT GOOD LOOKS LIKE:
  In Scope: "Transaction-level data for Regions A–E, Jan 2023–Jun 2024.
             Analysis covers revenue, return rates, and product category performance."
  Out of Scope: "Customer demographics and marketing spend data were excluded -
                 demographic data was incomplete for two regions, and marketing
                 data sits in a separate system outside this engagement."

  WHAT TO AVOID:
  ❌ Leaving Out of Scope blank. This is the section that protects your credibility.
     If you don't define the fence, reviewers assume you missed things.
-->

| Dimension | Details |
|-----------|---------|
| **In Scope** | Sales transaction data including revenue, product categories, regions, sales channels, and customer types |
| **Out of Scope** | Marketing spend data and customer demographics |
| **Time Period** | January – May 2025 |
| **Granularity** | Transaction-level sales data |

### Tools & Technologies

<!--
  List only what you actually used on this project.
  This is not your skills section - it's the project's technical context.
-->

| Category | Tool(s) Used |
|----------|-------------|
| Data Storage | Excel Dataset |
| Data Processing | Microsoft Excel |
| Analysis | Excel Pivot Tables |
| Visualization | Power BI |
| Version Control | [e.g., Git / GitHub] |
| Documentation | Git / GitHub |
| Other | Markdown |

---

## 4. Repository Structure

```
sales-performance-analysis/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── dashboard/
│   └── sales_dashboard.pbix
│
├── reports/
│   └── Sales_Performance_Report.pdf
│
├── presentation/
│   └── Sales_Performance_Presentation.pptx
│
├── visuals/
│   └── dashboard_preview.png
│
└── README.md

```
## 5. Data Workflow

```
Raw Sales Dataset
      ↓
Data Cleaning & Validation
      ↓
Feature Engineering
      ↓
Exploratory Data Analysis
      ↓
Dashboard Visualisation
      ↓
Business Insights & Recommendations
```

## Sales Performance Analysis 2025

### Source
Sales transaction dataset containing **2,098 transactions across four regions**.

### Ingestion
The dataset was imported into **Microsoft Excel** for preprocessing and transformation.

### Data Cleaning
The following checks were performed to ensure data quality:

- Checked for duplicate records *(none found)*
- Verified missing values
- Validated date formats
- Confirmed accuracy of **price** and **quantity** fields

### Data Transformation
New calculated fields were created to support analysis:

- **Revenue = Unit Price × Quantity**
- **COGS = Cost Price × Quantity**
- **Profit = Revenue − COGS**
- **Month Number**
- **Month Name**

The dataset expanded from **11 raw columns to 16 analytical columns** after transformation.

### Analysis
The analysis focused on identifying key business insights, including:

- Revenue distribution by **region**
- Profitability by **product category**
- Sales comparison across **sales channels**
- **Customer segmentation** analysis

### Output
The final deliverables include:

- **Power BI Interactive Dashboard**
- **Analytical Report**
- **Business Recommendation Presentation**

---

## 6. Data Model & Schema

<!--
  Define your fields so that someone reading your analysis can follow along
  without digging through your code.

  WHAT GOOD LOOKS LIKE (one row example):
  | transaction_id | string | Unique identifier per sales transaction | TXN-00482 |
  | return_flag    | boolean | Whether the transaction included a return | TRUE |
  | region_code    | string | Two-letter identifier for store region | "NE" |

  WHAT TO AVOID:
  ❌ Skipping this section because "the field names are self-explanatory."
     They're not. Not to a reviewer. Not to you in six months.

  📌 FOR SQL PROJECTS: If you have multiple tables, create one block per table.
     Describe join keys and relationships here. Your ERD (Section 7) will
     visualise what this section describes in text.

  📌 FOR NON-SQL PROJECTS: Describe the shape of your dataset informally
     if a formal schema doesn't apply. Even one paragraph is more helpful than nothing.
-->

### Dataset: `Sales Transactions`

| Field Name | Data Type | Description | Example Value |
|------------|-----------|-------------|---------------|
| `Transaction_ID` | Integer | Unique transaction identifier | 1023 |
| `Date` | Date | Transaction date | 2025-03-14 |
| `Region` | String | Sales region | East |
| `City` | String | Sales city | Lagos |
| `Customer_Type` | String | Retail or Corporate customer | Retail |
| `Sales_Channel` | String | Online or In-Store | Online |
| `Product_Category` | String | Product group | Electronics |
| `Product_Name` | String | Product sold | Laptop A13 |
| `Quantity` | Integer | Units sold | 3 |
| `Unit_Price` | Float | Price per unit | ₦450,000 |
| `Cost_Price` | Float | Cost per unit | ₦350,000 |
| `Revenue` | Float | Sales revenue | ₦1,350,000 |
| `COGS` | Float | Cost of goods sold | ₦1,050,000 |
| `Profit` | Float | Revenue minus cost | ₦300,000 |

> **Row count (approx.):** 2,098 transactions.

---

## 7. Analysis & Metrics

<!--
  Explain what you measured and how - before you share what you found.

  WHAT GOOD LOOKS LIKE:
  Metric: "Customer Return Rate"
  Definition: "Number of transactions flagged as returns divided by total
               transactions, calculated at product-category and regional grain."
  Why It Matters: "Return rate - not sales volume - was hypothesised to
                  explain regional revenue gaps. This metric tests that hypothesis."

  WHAT TO AVOID:
  ❌ Defining a metric only in code: SUM(returns) / COUNT(transaction_id)
     That's an implementation. Write the plain-language definition here.
     Both belong in your project - the definition in the README,
     the implementation in the code.
-->

### Analytical Approach

[Describe how you approached the analysis. Were you exploring patterns? Testing a hypothesis? Building and validating a pipeline? Be honest about your method - exploratory work is valid, just call it that.]

### Key Metrics Defined

| Metric | Plain-Language Definition | Why It Matters |
|--------|--------------------------|----------------|
| `Revenue` | Total sales generated | Measures overall business performance |
| `Profit` | Revenue minus COGS | Indicates profitability |
| `Profit Margin` | Profit ÷ Revenue | Measures operational efficiency |
| `Transaction Count` | Number of transactions | Indicates customer demand |

### Methods Used

- [e.g., Descriptive statistics - distribution, central tendency, outlier detection]
- [e.g., Trend analysis across [time period]]
- [e.g., Segmentation / group comparison by [dimension]]
- [e.g., Correlation analysis between [variable A] and [variable B]]
- [e.g., SQL window functions for [specific aggregation]]
- [e.g., Custom aggregation or transformation logic in [tool]]

---

## 8. Key Insights

<!--
  Findings + implications. Not just what happened - what it means.

  WHAT GOOD LOOKS LIKE:
  ✅ "Return rates, not sales volume, explain Region A's underperformance.
      Region A's return rate on home goods was 34% - more than double the
      company average. Revenue was not lost at the point of sale; it was
      lost post-sale through refunds. This points to a fulfilment or
      product quality issue specific to that region, not a demand problem."

  WHAT TO AVOID:
  ❌ "Region A had lower revenue than other regions in Q4."
     (That's an observation. It describes what happened.
      An insight says what it means and where to look next.)

  Aim for 3–6 insights. Quality over quantity.
-->

**Insight 1: Electronics products generate the highest profit**
Laptop A13 alone generated ₦105.3M profit, making it the top performing product.

**Insight 2: East region leads overall performance**
East region generated ₦643M revenue and ₦128.6M profit, outperforming other regions.

**Insight 3: In-Store remains the primary sales channel**
In-Store contributes 53% of total revenue, while Online accounts for 47%.

**Insight 4: Profit margin remains consistent across segments**
Both Retail and Corporate customers maintain roughly 20% profit margin, indicating stable pricing and cost structure.

---

## 9. Recommendations

<!--
  Action-oriented. Addressed to a real audience.
  Tied explicitly to the insight that supports each one.

  WHAT GOOD LOOKS LIKE:
  Priority: High
  Recommendation: "Conduct a fulfilment audit for home goods deliveries
                   in Region A - specifically investigating whether returns
                   correlate with a particular warehouse, carrier, or SKU batch."
  Based On: Insight 1 - return rate anomaly in Region A
  Owner: Operations / Supply Chain team

  WHAT TO AVOID:
  ❌ "Improve the return rate."
     (Not actionable. Doesn't say who, how, or where to start.)
  ❌ "Further analysis is needed."
     (This is a placeholder, not a recommendation.)
-->

| Priority | Recommendation | Based On | Suggested Owner |
|----------|---------------|----------|-----------------|
| High | Increase marketing for high-margin products (Laptop A13, Sofa Classic, Desktop PC D21) | Product profit analysis | Marketing Team |
| High | Expand online sales through digital campaigns | Channel performance analysis | Digital Marketing |
| Medium | Review pricing strategy for low-profit appliances | Product margin analysis | Product Management |
| High | Expand operations in East and West regions | Regional revenue analysis | Sales Strategy|

---

## 10. Assumptions & Limitations

<!--
  WHAT GOOD LOOKS LIKE:
  Assumption: "Sales data represents all transactions for the period.
               Product costs remained stable during the analysis period."
  Limitation: "Marketing spend data was not included
               May 2025 data is partial and not directly comparable to full months.
               Customer demographic data was unavailable"

  WHAT TO AVOID:
  ❌ Leaving this section blank or writing "None known."
     Every project has limitations. Documenting them is a sign of
     analytical maturity - not a confession of failure.
-->

### Assumptions
- Sales data represents all transactions for the period.
- Product costs remained stable during the analysis period.

### Limitations
- Marketing spend data was not included.
- May 2025 data is partial and not directly comparable to full months.
- Customer demographic data was unavailable.

---

## 11. Future Enhancements

<!--
  WHAT GOOD LOOKS LIKE:
  ✅ "Automate the monthly data pull from the POS export folder using
      a scheduled Python script, replacing the current manual process."
  ✅ "Expand the return rate analysis to include carrier-level data,
      which was unavailable in this dataset but exists in the logistics system."

  WHAT TO AVOID:
  ❌ "Add a machine learning model."
     (Vague, and disconnected from the actual findings of this project.)
  ❌ Listing aspirational features that don't follow logically from the work.
-->

- [ ] Build an automated sales dashboard with scheduled data refresh
- [ ] Incorporate marketing campaign data to analyse ROI
- [ ] Develop predictive models for future sales forecasting
- [ ] Expand analysis to cover full-year sales data

---

## 12. Deliverables

| Deliverable | Description | Location |
|-------------|-------------|----------|
| Power BI Dashboard | Interactive visualization of sales performance | /dashboard/ |
| Project Report | Detailed analysis and insights | /reports/ |
| Presentation | Business presentation of findings | /presentation/ |
| Dataset | Raw and processed sales dataset | /data/ |

---

## 13. Author

**Faith Adedolapo**
Data Analyst | Business Analyst

- 🔗 [LinkedIn URL](https://www.linkedin.com/in/faithadedolapoolayiwola)
- 💼 [Portfolio or GitHub profile URL](https://faithadedolapo.github.io/)
- 📧 [Email](olayiwolaadefaith@gmail.com)

---

*Last updated: [03 2026]*
