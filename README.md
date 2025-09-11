# Vendor Performance & Sales Analysis
An end-to-end data analysis project uncovering actionable insights into vendor performance, profitability, and inventory efficiency using Python, SQL, and Power BI.

This project transforms raw transactional data into a strategic dashboard for smarter business decision-making.

## About the Project
This project performs a comprehensive analysis of a sales and inventory dataset to evaluate vendor and brand performance.

The objective goes beyond simple sales metrics—it answers complex business questions around profitability, purchasing patterns, and inventory risk.
 

## ⚙️ Project Pipeline

```mermaid
flowchart TD
    A[Data Ingestion] --> B[Data Engineering]
    B --> C[Exploratory Data Analysis]
    C --> D[Statistical & In-depth Analysis]
    D --> E[Dashboarding & Insights]

    classDef step fill:#f5f5f5,stroke:#333,stroke-width:1px,rx:8,ry:8
    
    A:::step
    B:::step
    C:::step
    D:::step
    E:::step


## Business Problem

Effective inventory and sales management are critical for driving profitability in the retail and wholesale sectors. Companies face financial risks due to:

Inefficient pricing strategies

Poor inventory turnover

Overdependence on specific vendors

To mitigate these risks and uncover strategic insights, this analysis aims to:

🔍 Identify underperforming brands that may need promotional or pricing adjustments

📈 Determine top-performing vendors contributing most to sales and gross profits

📦 Analyze the impact of bulk purchasing on unit cost efficiency

🔄 Assess inventory turnover to minimize holding costs and maximize operational efficiency

📊 Investigate profitability gaps between high-performing and low-performing vendors

This project empowers data-driven decisions that optimize profitability, vendor management, and inventory operations across the business.
## 🛠️ Tech Stack

Data Ingestion & Transformation: Python (Pandas), SQL (SQLite)

Statistical Analysis: Python (NumPy, SciPy)

Visualization: Matplotlib, Seaborn

BI Dashboarding: Power BI, DAX

Environment: Jupyter Notebook

## Project Workflow

### Data Ingestion

Raw CSV files (sales, purchase, vendor data) ingested into a centralized SQLite database (ingestion_db.py).

### Data Engineering

Python script (get_vendor_summary.py) executes SQL queries with CTEs to join & aggregate data.

New calculated fields: GrossProfit, ProfitMargin, StockTurnover.

### Exploratory Data Analysis (EDA)

Conducted in Exploratory Data Analysis.ipynb.

Includes data validation, cleaning, and distribution checks.

In-Depth & Statistical Analysis

Main analysis in Vendor Performance Analysis.ipynb.

Applied hypothesis testing (t-tests), Pareto analysis, and segmentation.

Dashboarding

Cleaned dataset loaded into Power BI.

Built DAX measures and calculated tables for interactive visualizations.

## Key Analyses & Insights

### 1. Pareto Analysis: Vendor Purchase Contribution

Confirmed the 80/20 rule → ~80% of purchase dollars came from top 20% of vendors.

Helps prioritize strategic supplier relationships.

### 2. Profitability Analysis: High vs. Low Volume Sales

Hypothesis Test: Independent two-sample t-test.

Result: p-value < 0.05 → significant difference.

Conclusion: Low-volume sales generate higher profit margins → strong premium/niche strategy.

### 3. Niche Brand Identification

Scatter plot of sales volume vs. profit margin.

DAX calculated column flags “Target Brands” in bottom 15% of sales but top 15% of profitability.

Identified as “niche champions” with high growth potential.

### 4. Inventory Risk & Unsold Capital

Calculated total capital tied up in unsold stock.

Bar chart highlights top 10 vendors with highest slow-moving inventory.

Informs supply chain risk management.

## Outcomes
Delivered a centralized analytical dataset integrating sales, purchase, and inventory.

Created interactive Power BI dashboard for executives.

Produced statistically validated insights supporting vendor prioritization and inventory optimization.
