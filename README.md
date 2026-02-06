# Sales Intelligence Dashboard – Geographic, Customer & Product Performance Analysis

This portfolio project uses synthetic data designed to replicate a real-world business environment (fictional company "Plant Co."). The dataset models transactional sales activity across customers, products, and geographic locations, enabling end-to-end analysis of commercial performance, customer behavior, product portfolio effectiveness, and sales trends. Exploratory Data Analysis (EDA) is performed to discover performance drivers, identify growth opportunities, and highlight areas of underperformance across markets and customer segments. This project is produced in its entirety solely using MS Power BI.

## Table of Contents

- [Target Users](#target-users-executive-leadership-sales-management--business-stakeholders)
- [Understanding the Data](#understanding-the-data)
- [Data Analysis Framework](#data-analysis-framework)
- [Analytical Focus & Key Business Questions](#analytical-focus--key-business-questions)
- [Key Insights & Strategic Action Recommendations](#key-insights--strategic-action-recommendations)
  - [Interactive Dashboard](#intearactive-dashboard)
  - [Question 1 – Geographic Performance](#question-1-insights-and-recommendations)
  - [Question 2 – Customer Value & Revenue Concentration](#question-2-insights-and-recommendations)
  - [Question 3 – Product Portfolio Performance](#question-3-insights-and-recommendations)
  - [Question 4 – Sales Trends & Seasonality](#question-4-insights-and-recommendations)
  - [Question 5 – Account–Product Value Creation](#question-5-insights-and-recommendations)


## Target Users: Executive Leadership, Sales Management & Business Stakeholders

This analysis is designed for business leaders and commercial stakeholders seeking to optimize sales performance and drive sustainable growth through data-driven decision-making. It delivers actionable insights into geographic performance, customer value creation, product portfolio effectiveness, pricing and margin dynamics, cross-sell opportunities, and long-term sales trends and seasonality.

## Understanding the Data

The data for this project consists of three sperate spreadsheets: Dim_Account, Fact_Sales, Dim_Product

<table>
<tr>
<td valign="top">

**Dim_Account Table**

| Column Name  | Data Type  |
|--------------|------------|
| country_code | Text       |
| Account      | Text       |
| Master_id    | Number     |
| Account_id   | Text       |
| latitude2    | Number     |
| longitude    | Number     |
| country2     | Text       |
| Postal_code  | Text       |
| street_name  | Text       |
| Street_number| Number     |

</td>
<td valign="top">

**Fact_Sales Table**

| Column Name   | Data Type  |
|---------------|------------|
| Product_id    | Number     |
| Sales_USD     | Number     |
| quantity      | Number     |
| Price_USD     | Number     |
| COGS_USD      | Number     |
| Date_Time     | Date       |
| Account_id    | Text       |

</td>
<td valign="top">

**Dim_Product Table**

| Column Name      | Data Type  |
|------------------|------------|
| Product_Family   | Text       |
| Product_Family_Id| Number     |
| Product_Group    | Text       |
| Product_Group_Id | Number     |
| Product_Name     | Text       |
| Product_Size     | Text       |
| Product_Type     | Text       |

</td>
</tr>
</table>

Data processing will be applied in Microsoft Power BI. For more information, please read the Data Analysis Framework section below.

## Data Analysis Framework

The following set of cleaning and transformation steps was implemented in this project: 

* Data preprocessing - formatting data nad column names using DAX for consistency, readability and applicability
* Duplicate checking and removal from unique identifiers
* Building VIRTUAL TABLES, CALCULATED COLUMNS and MEASURES
* Setting up RELATIONS between different datasets in model back-end

Next stages involve: 1) data visualisation by producing dynamic, interactive dashboards in MS Power BI using SLICERS, CARDS, CONDITIONAL FORMATTING and multiple CHARTS (TREEMAP, WATERFALL, COMBO and SCATTER); and 2) data storytelling by delivering a comprehensive analysis report using MS PowerPoint. The output of both steps is available in the GitHub repository under 'PowerBI_Portfolio_Project.pbix' and 'Stakeholder report.pptx', respectively.

## Analytical Focus & Key Business Questions

This section contains questions important to people from different teams in the fictional company, including 1) Senior Management; 2) Commercial & Sales Management; 3) Finance & Business Performance; and 4) Strategy & Business Intelligence. According to them, worth exploring and may provide insights into commercial performance, enabling data-driven strategies across sales growth, customer management, product optimization, and geographic expansion.

List of business-related enquiries and their relevance:

1. *Which countries, regions, and specific locations generate the highest sales and profit?* => Helps leadership prioritise geographic expansion, marketing spend, and sales coverage. 

2. *Which accounts drive the most revenue and profitability, and how concentrated is our sales base?* => Supports key account strategy, customer risk management, and sales prioritisation.

3. *Which product families and groups contribute most to revenue, volume, and margin?* => Informs product strategy, portfolio optimisation, and investment decisions.

4. *How do sales trends evolve over time, and are there seasonality patterns?* => Enables forecasting, inventory planning, and resource allocation.

5. *Which product–account combinations create the most value?* => Supports cross-sell, upsell, and account-based selling strategies.

## Key Insights & Strategic Action Recommendations

This section presents a concise overview of the patterns and trends revealed through Exploratory Data Analysis (EDA) in relation to each of the questions posed above, followed by recommendations derived from the findings.

### Interactive dashboard 
![image](https://github.com/user-attachments/assets/9343d514-e759-4001-abc3-774ea5ece85e)

### Question 1 Insights and recommendations

**Key Insights:** 

* China and France together represent the largest volume declines, signaling urgent performance risks.
  
* Multiple European and Asian markets are simultaneously underperforming, indicating systemic regional challenges rather than isolated issues.
  
* Overall positive YTD growth is driven by a limited number of strong-performing countries, increasing concentration risk.
  
* Geographic imbalance suggests missed revenue opportunities and suboptimal market penetration in key regions.

**Based on this analysis, I recommend the following actions:**

* Conduct deep-dive root cause analysis in China and France focusing on pricing, competition, customer churn, and supply chain performance.
  
* Launch targeted commercial recovery plans for underperforming countries, including tailored promotions, product mix adjustments, and key account interventions.
  
* Strengthen regional sales execution and distributor performance management.
  
* Reallocate marketing and sales investments toward high-potential recovery markets to rebalance geographic contribution.

### Question 2 Insights and recommendations

**Key Insights:** 

* Customer value is highly concentrated, with a small number of accounts driving a large share of volume and gross profit.

* A meaningful portion of volume originates from low-margin accounts, increasing profitability risk.

* High-volume, low-margin customers indicate pricing inefficiencies and discount dependency.

* The long tail of low-value customers contributes to operational inefficiency and margin dilution.

**Based on this analysis, I recommend the following actions:**

* Develop tiered account strategies, prioritising investment and service for high-value strategic customers.
* Implement pricing optimisation and discount governance frameworks for high-volume, low-margin accounts.
* Launch targeted cross-sell and upsell campaigns for low-volume, high-margin customers.
* Review and streamline service models for low-value accounts to reduce cost-to-serve.

### Question 3 Insights and recommendations

**Key Insights:** 

* Sales volume is concentrated in Outdoor and Landscape product types.
  
* Product demand displays strong seasonal patterns, particularly in the second and third quarter of the year.
  
* Indoor products provide more stable year-round performance but remain under-leveraged.
  
* Product mix imbalance increases forecasting, inventory, and operational risk.
  
* Portfolio performance is exposed to seasonality-driven volatility.

**Based on this analysis, I recommend the following actions:**

* Expand Indoor product ranges and promotions to strengthen non-seasonal demand.
* Introduce product bundling strategies that combine seasonal and non-seasonal items to stabilise revenue.
* Implement seasonality-adjusted inventory planning models.
* Optimise product lifecycle management, focusing investment on high-growth, high-margin categories.

### Question 4 Insights and recommendations

**Key Insights:** 

* Business performance exhibits strong seasonal fluctuations.
  
* Growth is heavily concentrated in the second and early third quarter.
  
* Early and late-year months consistently underperform.
  
* Overall positive YTD growth masks significant intra-year volatility.
  
* Current trends increase forecasting complexity and planning risk.

**Based on this analysis, I recommend the following actions:**

* Implement seasonality-adjusted forecasting models.
* Launch off-season demand stimulation campaigns, such as targeted promotions and bundled offerings.
* Optimise inventory and production planning cycles around peak and trough demand periods.
* Introduce flexible staffing and logistics models to scale efficiently across seasonal demand shifts.
* Build seasonality Key Performance Indicators (KPI) to track volatility, growth stability, and forecast accuracy.

### Question 5 Insights and recommendations

**Key Insights:** 

* High-value customers exhibit strong product–account alignment.

* High-volume, low-margin accounts indicate missed cross-sell and upsell opportunities.

* Low-volume, high-margin customers represent scalable growth potential.

* Product mix optimisation at account level is a critical lever for margin improvement.

* Systematic cross-sell strategies can materially increase customer lifetime value.

**Based on this analysis, I recommend the following actions:**

* Develop account-level product affinity models to guide cross-sell targeting.
* Implement structured cross-sell playbooks for strategic and growth accounts.
* Introduce incentive mechanisms aligned to margin and product mix improvement, not just volume.
* Deploy personalised product recommendations within sales planning and Customer Relationship Management (CRM) workflows.
* Establish account-product Key Performance Indicators (KPI) to track mix quality, margin uplift, and cross-sell conversion.
