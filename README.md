# MULTI-PURPORSE SALES ANALYSIS

# Exploratory Data Analysis (EDA) - multi-purpose Sales Performance Data

**Project Overview**

In this project, we conducted an Exploratory Data Analysis (EDA) on retail sales data to uncover key insights that could drive business decisions. The dataset includes Fical periods, models, markets e.t.c.

**Key Objectives:**

- Understand Sales Distribution: Analyze total sales across different products, regions, and time periods. 

-Identify Trends: top 10 highest selling stores.

-Highlight Top Performers: Determine the highest-selling products and regions. 

-Spot Underperformance: Identify products with declining or no sales in recent periods.

# DATA SOURCE
The primary dataset used for this analysis is the "LITA data set BI visualization".

# Steps and Insights:
--- Data Cleaning and Preparation

--- Checked for missing values and duplicates, ensuring data integrity. 

--- Standardized date formats for temporal analysis.

### Summary Statistics 

Generated summary statistics to understand the distribution of key metrics like total sales, average revenue per product, and transactions by region.

# Sales Analysis

--- Total Sales by Product: Identified the top-selling line of business.

---Revenue by Region: Highlighted which regions contribute most to total sales.




-Power BI Dashboard: download here

The final deliverable Built an interactive dashboard for visual storytelling and real-time analysis, designed to visualize sales segments, Monthly sales trends, total revenue, region e.t.c. Key performance indicators (KPI cards) highlighted essential metrics like total revenue, top regions for sales,

data analysis queries:
=F3*G3
SELECT PRODUCT, SUM(QUANTITY*UNITPRICE) AS TOTALSALES
FROM [dbo].[sales data pro dupli removedd]
GROUP BY PRODUCT
SELECT REGION, COUNT(ORDERID) AS
NUMBER_OF_TRANSACTIONS
FROM [dbo].[sales data pro dupli removedd]
GROUP BY REGION
SELECT PRODUCT, SUM(QUANTITY*UNITPRICE) AS TOTALSALES
FROM [dbo].[sales data pro dupli removedd]
GROUP BY PRODUCT
ORDER BY TOTALSALES DESC;
SELECT PRODUCT, SUM(QUANTITY*UNITPRICE) AS TOTALSALES
FROM [dbo].[sales data pro dupli removedd]
GROUP BY PRODUCT
SELECT DATEPART(MONTH,ORDERDATE) AS MONTH,
SUM(QUANTITY*UNITPRICE)AS
TOTALSALES
FROM [dbo].[sales data pro dupli removedd]
WHERE DATEPART(YEAR, ORDERDATE)
=YEAR(GETDATE())
GROUP BY DATEPART (month,ORDERDATE);
SELECT TOP 5 CUSTOMER_ID,
SUM(QUANTITY*UNITPRICE) AS
TOTALPURCHASE
FROM [dbo].[sales data pro dupli removedd]
GROUP BY CUSTOMER_ID 
ORDER BY SUM(QUANTITY*UNITPRICE) DESC;
SELECT REGION, 
(SUM(QUANTITY*UNITPRICE) * 100.0)/(SELECT SUM(QUANTITY*UNITPRICE)
FROM [dbo].[sales data pro dupli removedd])
AS SALESPERCENTAGE
FROM [dbo].[sales data pro dupli removedd]
GROUP BY REGION;
select product
from [dbo].[sales data pro dupli removedd]
where orderdate>
dateadd(quarter,-1, getdate())
group by product
having sum(quantity)=0;
Visuals and Dashboard
Sales Overview: Showcased total sales, revenue trends, and regional performance.
Top Products: Bar charts displaying the best-selling products.
Regional Breakdown: Pie charts and maps highlighting sales distribution by region.
Result
Sales Fluctuations:

Notable fluctuations were observed in the monthly sales trends for both 2023 and 2024. These variations could be attributed to seasonal demand changes, promotional activities, or market conditions. Top Selling Products:
Shirts:

Shirts emerged as the highest-selling product, generating the most sales overall. The South region was identified as the primary contributor to shirt sales, reflecting strong demand in this area.
Hats:

Hats recorded the highest count in sales transactions, indicating a high volume of purchases. Despite the high sales count, hats ranked third in total revenue generated. This suggests a lower price point compared to shirts or the influence of discounts on overall sales.
Recommendation
My Recommendations Based on Sales Analysis are:

Focus Marketing Efforts on SHIRT:
Since SHIRT is the top-selling product and contributes significantly to revenue, particularly boosted by sales in the South region, consider increasing marketing and promotional activities in this area. Special promotions or campaigns focused on SHIRT could further enhance its performance. Explore potential for upselling or bundling SHIRT with other products, like HAT, to increase the overall basket size per customer.

Leverage South Region's Sales Strength:
With the South region leading in total sales, this area shows high customer engagement and demand. Invest in regional-specific marketing campaigns, such as localized advertisements, events, or discounts. Strengthen supply chain logistics and inventory management in the South to prevent stockouts and ensure customer demand is met promptly.

Address HAT's Performance Gap:
Although HAT has a higher sales count, it lags in revenue generation. This discrepancy suggests a need to either re-evaluate the pricing strategy for HAT or focus on improving its value perception among customers. Consider product enhancements or introducing premium versions of HAT to boost revenue per unit sold.

Stabilize Monthly Sales Fluctuations:
The fluctuating sales trend indicates varying customer demand across months. Implement data-driven demand forecasting and inventory planning to align stock levels with expected sales patterns. Identify and analyze months with higher sales to understand the drivers behind the spike. Leverage these insights to replicate successful strategies in slower months. Introduce targeted marketing campaigns during historically low-performing months to stimulate demand, possibly tied to events, holidays, or special promotions.

Continuous Monitoring and Adaptation:
Regularly review sales data to detect emerging trends or shifts in customer behavior. Agile response to changing dynamics can help maintain and potentially grow sales performance across regions and products. Consider launching loyalty programs or customer feedback initiatives to deepen customer relationships and gather actionable insights for further product or service improvements.




