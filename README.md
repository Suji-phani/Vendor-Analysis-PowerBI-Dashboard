Vendor Performance & Sales Analysis
An end-to-end data analysis project to uncover actionable insights into vendor performance, profitability, and inventory efficiency using Python, SQL, and Power BI. This project transforms raw transactional data into a strategic dashboard for business decision-making.

[Link to Dashboard Image]

📝 About The Project
This project performs a comprehensive analysis of a sales and inventory dataset to evaluate vendor and brand performance. The primary objective is to move beyond simple sales metrics and answer complex business questions related to profitability, purchasing patterns, and inventory risk.

The project pipeline begins with ingesting raw data files, followed by an intensive data engineering phase using SQL and Python to create a unified analytical dataset. In-depth exploratory and statistical analyses are then conducted in Jupyter Notebooks. The final, actionable insights are presented in an interactive Power BI dashboard.

 Key Business Questions Addressed:

Who are the top vendors by sales and overall purchase contribution?

How does bulk purchasing impact per-unit costs?

Is there a statistically significant difference in profit margins between high-volume and low-volume sales?

Which vendors are most associated with slow-moving inventory and locked-up capital?

Can we identify "niche champion" brands with low sales volume but high profitability?

 Tech Stack
Data Ingestion & Transformation: Python (Pandas), SQL (SQLite)

Statistical Analysis: Python (NumPy, SciPy)

Data Visualization: Matplotlib, Seaborn

BI Dashboarding: Power BI, DAX

Environment: Jupyter Notebook

⚙️ Project Workflow
The project follows a structured, multi-stage data analysis workflow:

Data Ingestion: Raw CSV files containing sales, purchase, and vendor data are automatically ingested into a centralized SQLite database using the ingestion_db.py script.

Data Engineering: A robust Python script (get_vendor_summary.py) executes a complex SQL query with Common Table Expressions (CTEs) to join and aggregate data. It then enriches the dataset by creating new calculated columns (e.g., GrossProfit, ProfitMargin, StockTurnover).

Exploratory Data Analysis (EDA): The Exploratory data Analysis.ipynb notebook is used for initial data validation, cleaning, and understanding distributions and relationships.

In-depth & Statistical Analysis: The core analysis is performed in the Vendor Performance Analysis.ipynb notebook. This includes statistical hypothesis testing (t-tests), Pareto analysis, and segmentation.

Dashboarding: The final, cleaned dataset is loaded into Power BI, where DAX measures and calculated tables are created to build interactive visuals that present the key findings.

📊 Key Analyses and Insights
1. Pareto Analysis: Vendor Purchase Contribution

A Pareto chart was created to confirm the 80/20 rule, revealing that approximately 80% of the total purchase dollars come from the top 20% of vendors. This helps prioritize relationship management with key suppliers.


Licensed by Google
2. Profitability Analysis: High-Volume vs. Low-Volume Sales

A statistical hypothesis test (independent two-sample t-test) was conducted to compare profit margins.

Null Hypothesis (H₀): There is no significant difference in the mean profit margins of top-performing and low-performing vendors.

Result: The test yielded a p-value < 0.05, leading to the rejection of the null hypothesis.

Conclusion: Low-volume sales transactions generate a statistically significant higher profit margin than high-volume sales, suggesting a successful premium or niche product strategy.

3. Niche Brand Identification

A scatter plot visualizes all brands based on their sales volume and average profit margin. A DAX calculated column flags "Target Brands" that fall in the bottom 15% of sales but the top 15% of profitability, identifying them as "niche champions" with high growth potential.

4. Inventory Risk & Unsold Capital

The analysis calculated the total capital locked in unsold inventory, aggregated by vendor. A bar chart identifies the top 10 vendors associated with the highest value of slow-moving stock, highlighting potential risks in the supply chain.


