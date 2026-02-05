# Sales Intelligence Dashboard – Geographic, Customer & Product Performance Analysis

This portfolio project uses synthetic data designed to replicate a real-world business environment (fictional company "Plant Co."). The dataset models transactional sales activity across customers, products, and geographic locations, enabling end-to-end analysis of commercial performance, customer behavior, product portfolio effectiveness, and sales trends. Exploratory Data Analysis (EDA) is performed to discover performance drivers, identify growth opportunities, and highlight areas of underperformance across markets and customer segments. This project is produced in its entirety solely using MS Power BI.

## Table of Contents

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
