# FMCG Net Revenue Management in Excel
Analyzed FMCG data to optimize pricing, product mix, and promotional strategies, enhancing net revenue management. Tracked sales and market performance by analyzing KPIs. Calculated yearly growth, month-to-month, YTD and MAT.  

## Project Overview



  In today’s ultra-competitive FMCG arena, data-driven insights are the secret weapon behind the success of iconic brands like Coca-Cola, Nivea, and Lay’s. This project harnesses the power of advanced Excel analytics to transform raw market data into actionable, high-impact business strategies for HealthMax, a market leader in the shampoo industry. By combining rigorous data analysis with strategic forecasting, this project illuminates pathways to superior revenue growth and profitability.



## Data Analysis & Methodology 

### 1. Market Performance & Brand Growth



The journey begins with a meticulous examination of HealthMax’s market performance. Using dynamic PivotTables, I aggregated value sales data from 2018 to 2022, revealing compelling insights into brand evolution and year-over-year growth—while deliberately excluding the incomplete 2023 data to maintain accuracy.

![2025-03-30](https://github.com/user-attachments/assets/79d36117-4b6f-4116-aafe-e609a5aede9f)

📊 Notable Insight: HealthMax had it's strongest year of growth in 2020 at nearly 4%. Shinez was a big contributor with 7.7% growth!



### 2. Year-to-Date (YTD) & Moving Annual Total (MAT) Analysis



To capture both seasonal nuances and long-term trends, I calculated:

• YTD Sales: Using SUMIFS() to track cumulative performance. (=SUMIFS(I:I,D:D,[@Brand],E:E,[@Region],F:F,[@Year];G:G,"<="&[@Month]))

• MAT: A moving annual total that smooths seasonal volatility, offering a robust view of the latest 12-month performance. (=[@[Values YTD]]+SUMIFS(I:I;D:D;[@Brand];E:E;[@Region];F:F;[@Year]-1;G:G;">"&[@Month]))


![2025-03-30 (1)](https://github.com/user-attachments/assets/b90ca3d9-37eb-465b-8e43-1e7f5369aae6)

📊 Notable Insight: In the most recent 12 months, the shampoo's generated over $98 million of turnover.





### 3. Profitability & Gross Margin Optimization



Profitability is the heartbeat of strategic decision-making. Here, I dissected product-level performance by calculating:

• Net Sales per Product (Net Price x Volume 2022)

• Gross Profit per Unit (Net Price - COGS) 

• Gross Profit per product  (Gross Profit per unit x Volume 2022)

• Gross Margin  (Gross Profit per unit / Net Price)

• Profitability Matrix: A scatter plot mapping gross margin against net sales contribution, spotlighting the stars in the portfolio.

![2025-03-30 (7)](https://github.com/user-attachments/assets/ad07c00f-6b49-4e29-8522-9bfc72226d44)

📊 Notable Insight: Starbust Ultra Soft 100ML emerged as the flagship product, while Shinez Repair 200ML demonstrated unparalleled profitability.





### 4. New Category Expansion: Organic Shampoo



Since HealthMax is only active in 2 out of the 5 shampoo subcategories, it would be interesting to launch a new product to enter a new subcategory. To do this, I identified the fastest growing subcategory (in units). 

![2025-03-30 (3)](https://github.com/user-attachments/assets/f1d883e3-615d-4448-a6b1-19a7794ef4c7)

📊 Notable Insight: Organic is by far the fastest growing subcategory from 2018 to 2022 at 276%!

Once I knew the fastest growing subcategory, I made a full year estimate for the amount of units in the organic subcategory in 2024. First, we want to look at the latest yearly size of this subcategory, using the Units MAT values for March 2023, which is the latest data available. 

Based on this histoic trend, the 2024 category size should be approximately 20% higher than the March 2023 MAT values. (We multiply Units MAT of Organic by 1.2)

![2025-03-31](https://github.com/user-attachments/assets/cdb33aa7-4877-410c-8226-445539d98a43)

📊 Notable Insight: Projected 2024 Potential:  1,02 million units in the organic category are expected to sell in 2024.


### 5. Pricing Strategy: 50ML Shampoo Pack Launch



Capitalizing on consumer demand for travel-sized options, I reengineered the pricing strategy:

• Calculated Price per ML: Based on the existing 100ML product to determine a competitive 50ML retail price.

• Sales Volume Forecast: Estimated the 50ML variant’s sales at 10% of the 100ML pack’s 2022 volume, ensuring a viable market entry.

📊 Notable Insight: The 50ML pack is projected to generate significant annual net sales, unlocking a new revenue stream.

![2025-03-30 (6)](https://github.com/user-attachments/assets/98aa6646-8217-4e68-b10e-a4813895a532)

![2025-03-30 (5)](https://github.com/user-attachments/assets/51763028-42e4-42b1-82dc-451fdd6e9318)



### 6. Promotional Effectiveness & ROI Analysis



To refine our promotional strategies for 2024, I evaluated three past promotions on the Shinez brand by:

• Establishing Baseline Sales & Calculating Uplift: Using VLOOKUP() and PivotTables.

• Computing ROI: Determining the efficiency of each promotion to isolate the most cost-effective strategy.

📊 Notable Insight: One promotion emerged as the clear winner in terms of ROI, setting the benchmark for future campaigns.



![2025-03-30 (8)](https://github.com/user-attachments/assets/a66c0cf4-1232-44f6-8772-dfdfd4c60a5d)




### 7. Revenue Forecasting & Waterfall Growth Model



The final phase synthesizes all insights into a compelling forecast:

• Market Sales Forecast: Using historical data and Excel’s forecasting tools to predict 2023 and 2024 market values.

• Net Sales Projection: Applying established market ratios to estimate HealthMax’s net sales.

• Waterfall Analysis: A visual model that integrates natural growth, new product initiatives, and the 50ML launch to reveal the total revenue impact.

📊 Notable Insight: The comprehensive forecast projects a significant boost in 2024 revenue, affirming the effectiveness of the combined NRM initiatives.


![2025-03-30 (9)](https://github.com/user-attachments/assets/583eec6f-648d-4ba6-8770-f1471b726422)

---

![2025-03-30 (10)](https://github.com/user-attachments/assets/07d43c43-beba-43b9-a1ff-c7cf495f40db)
