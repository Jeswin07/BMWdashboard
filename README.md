  Project Overview
  
BMW Global Performance Insights is a Power BI project focused on analyzing BMW’s global sales to uncover performance patterns, highlight regional trends, and deliver clear, actionable insights using data storytelling principles.
The report follows the Introduction → Conflict → Resolution narrative model, transforming raw sales data into meaningful business decisions.


  Objectives
  
Analyze BMW’s worldwide sales performance across regions and years.
Identify top-performing models and high-performing markets.
Visualize sales growth trends and YOY (Year-over-Year) performance.
Apply design & storytelling principles for clarity and insight.
Ensure ethical, transparent, and accessible data visualization practices.


  Data Modeling
  
The data model uses a Star Schema:
Fact Table: fact_Sales
Dimension Tables: dim_model, dim_channel, dim_Calender, dim_country
Key Relationships:
ModelID → dim_model
ChannelID → dim_channel
Date → dim_Calender
CountryID → dim_country
This structure ensures efficient filtering, aggregation, and reporting.


  Visualizations & Insights
  
Page 1 – Introduction: Global Overview
https://github.com/Jeswin07/BMWdashboard/blob/main/BMW%20Global%20Overview.png
Purpose: High-level snapshot of BMW’s worldwide sales performance (2020–2024).

Highlights:
Global sales distribution map
KPIs: Top Region, Total Units, Total Revenue
Sales by Region & Channel
Sales & Units by Year (Growth patterns)

Answers:
 “How has BMW performed globally, and which regions lead the market?”

Page 2 – Conflict: Regional & Model Insights

Purpose: Deep dive into model, market, and revenue trends.

Highlights:
Revenue vs. Previous Year (+24.7% growth)
Top Selling and Most Expensive Models
Country-wise sales table with flags
Quantity Sold by Sales Channel

Answers:
“Which models and markets drive BMW’s performance?”

Page 3 – Resolution: Model Performance

Purpose: Detailed view of a selected model’s performance across regions & years.

Highlights:
Dynamic model image
Average Price KPI
Total Sales by Region (USD)
Yearly performance table (2020–2024)
Interactive model selector carousel

Answers:
“How does each BMW model perform across markets and time?”

Design & Storytelling Principles
Clear typography hierarchy
Soft contrasting color palette
Consistent spacing & alignment
White space for readability
Custom neutral background for clean presentation
Emphasis on narrative flow through all report pages


  Key DAX Measures
  
Measure	Formula	Purpose
Total Sales	SUM(fact_Sales[Revenue])	Total revenue
Total Quantity	SUM(fact_Sales[UnitsSold])	Total units sold
YOY Growth	([Revenue] - [Revenue PY]) / [Revenue PY]	Year-over-year comparison
Revenue PY	CALCULATE([Revenue], DATEADD(dim_Date[Date], -1, YEAR))	Previous year's revenue
Sales Rank	RANKX(ALL(dim_Products[ProductName]), [Total Sales], , DESC)	Model ranking
Formatted Revenue	FORMAT([Revenue]/1000000, "$0.0M")	Revenue in millions


  Ethical & Accessibility Considerations
  
Avoided 3D charts and visual clutter
Accurate scale representation
Transparent labels, legends, and filter indicators
Colorblind-friendly palette for accessibility
Clean, interpretable visuals for unbiased reporting


  Tools & Environment
  
Tool / Software	Purpose
Power BI Desktop	Data modeling, DAX, dashboard creation
Excel/CSV	Source data & initial preprocessing
Power Query	ETL: Cleaning & transforming data


  Conclusion
  
The BMW Global Performance Insights Dashboard transforms complex sales data into a compelling narrative that helps decision-makers:
Understand global sales performance
Identify high-growth and underperforming regions
Analyze model-level contributions
Plan strategic initiatives backed by data
This project demonstrates the power of combining data modeling, visualization, and storytelling to drive meaningful business insights.


  Author
  
Created by: Jeswin K R
Tool: Microsoft Power BI Desktop
Date: October 2025
