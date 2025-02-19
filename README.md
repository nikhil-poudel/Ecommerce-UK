# Project Background
This project will be using the transactional data for a UK e-commerce retail site. The company mainly sells unique all-occasion gifts with customers primarily being wholesalers.

We will throughly analyze and synthesize the data provided to uncover critical insights and provide valuable recommendations to increase their commercial success.

Insights and recommendations will be provided in the following areas: 
* Sales Trends Analysis: Evaluation of sales patterns with a focus on Revenue, Order Volume, and Seasonal Trends.
* Inventory Management Analysis: Providing recommendations on when to start stocking certain seasonal items along with recommendations on the prioritization of certain items.
* Customer Profile Analysis: Analysis of customer purchasing behavior to better understand what products were bought together most frequently and what product descriptors interested customers the most.
* Product Performance: Evaluation of product performance throughout the year and in different regions.

An interactive Tableau Dashboard can be found [HERE].

The Python code used to clean, analyze, and transform the data can be found [HERE].

### Basic Overview of the Data
The uncleaned and unaltered data can be found [HERE].

The cleaned and transformed data can be found [HERE].

The unaltered data consists of 8 columns: InvoiceNo, StockCode, Description, InvoiceDate, Quantity, UnitPrice, CustomerID, and Country. It has a total row count of 541,910 rows.

The transformed data separates the InvoiceDate into Month, Day of the Week, and Time of Purchase. It also adds a column for totals by multiplying Quantity and Unit price. It has a total row count of [INSERT ROW COUNT] rows.

The transformed data consists of 11 columns: InvoiceNo, StockCode, Description, Quantity, UnitPrice, CustomerID, Country, Year, Day, Time, and Totals. 

# Executive Summary

### Overview of Findings 
Unsurprisingly, the company's peak revenue was achieved during the latter half of the year, approaching Christmas. Surprisingly though, this increase in revenue starts in September which experiences a 33% boost in revenue and a 25% increase in order volume compared to August. Though this is the largest percentwise change between months; overall revenue and order volume peaks in November with a 26% increase in revenue and a 23% increase in order volume compared to October. We'll explore below on how we can further capitalize on this trend and use customer purchasing behavior displayed during this time to try and increase revenue during other parts of the year.


### Sales Trends
* The company achieved an overall revenue of £9,747,747.93 in this timeframe with 22,061 orders. 
* Company sales peaked in November with 3,021 orders totaling £1,461,756.25 in monthly revenue, corresponding with proximity to the holidays in December.
* Though sales dropped in December, it was still the second highest in the year with 2,568 orders totaling £1,182,625.03 in revenue.
* Other holidays did not reach anywhere near these peaks, with February having the lowest order volume at 1,174 and second lowest earnings at £498,062.65 despite Valentine's Day being a gift-giving holiday.

![image](https://github.com/user-attachments/assets/13022da4-44dc-4df7-9ded-79bc0a9a5816)


### Customer Profile Analysis
* Using Machine Learning algorithms, we were able to analyze customer purchasing behavior to identify the most popular product combinations.
* For example, the most popular combination was the Jumbo Bag Pink Polkadot and Jumbo Bag Red being present in 4.1% of all orders.
* Using this, we can target product recommendations to facilitate cross-selling, below is a useful heatmap that shows some of our most popular combinations which can be used in that regard.

![image](https://github.com/user-attachments/assets/33dcb6be-db8a-4217-aa03-2b7489f09031)

* Another key insight we uncovered was that certain products had a much higher probability of being bought together, rather than separately.
* These indicate strong relationships between products which can be leveraged through marketing strategies like product bundling.
* The value we're looking at is a ratio, so any number higher than 1 is a great sign of a meaningful relationship.

![image](https://github.com/user-attachments/assets/e0998d44-a7bc-4a99-bf33-61d9d82aea40)


