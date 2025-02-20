# Project Background
This project will be using the transactional data for a UK e-commerce retail site. The company mainly sells unique all-occasion gifts with customers primarily being wholesalers.

We will throughly analyze and synthesize the data provided to uncover critical insights and provide valuable recommendations to increase their commercial success.

Insights and recommendations will be provided in the following areas: 
* Sales Trends Analysis: Evaluation of sales patterns with a focus on Revenue, Order Volume, and Seasonal Trends.
* Inventory Management: Providing recommendations on when to start stocking certain seasonal items along with recommendations on the prioritization of certain items.
* Customer Profile Analysis: Analysis of customer purchasing behavior to better understand what products were bought together most frequently and what product descriptors interested customers the most.
* Product Performance: Evaluation of product performance throughout the year and in different regions.

An interactive Tableau Dashboard can be found [HERE].

The Python code used to clean and transform the data can be found in the following notebook [here] (Ecommerce_UK_Cleaning.ipynb).

The Python code used to analyze the data with ML Functions can be found in the following notebook [here] (Ecommerce_uk_MLFunctions.ipynb).

### Basic Overview of the Data

The unaltered data can be downloaded [here](ecommerceUK_RAW.rar).

The cleaned and transformed data can be downloaded [here](ecommerceUK_CLEANED.rar).

The unaltered data consists of 8 columns: InvoiceNo, StockCode, Description, InvoiceDate, Quantity, UnitPrice, CustomerID, and Country. It has a total row count of 541,910 rows.

The transformed data separates the InvoiceDate into Month, Day of the Week, and Time of Purchase. It also adds a column for totals by multiplying Quantity and Unit price. It has a total row count of 530,693 rows.

The transformed data consists of 11 columns: InvoiceNo, StockCode, Description, Quantity, UnitPrice, CustomerID, Country, Year, Day, Time, and Totals. 

# Executive Summary

### Overview of Findings 
Unsurprisingly, the company's peak revenue was achieved during the latter half of the year, approaching Christmas. Surprisingly though, this increase in revenue starts in September which experiences a 33% boost in revenue and a 25% increase in order volume compared to August. Though this is the largest percentwise change between months; overall revenue and order volume peaks in November with a 26% increase in revenue and a 23% increase in order volume compared to October. We'll explore below on how we can further capitalize on this trend and use customer purchasing behavior displayed during this time to try and increase revenue during other parts of the year.


### Sales Trends
* The company achieved an overall revenue of £9,747,747.93 in this timeframe with 22,061 orders. 
* Company sales peaked in November with 3,021 orders totaling £1,461,756.25 in monthly revenue, corresponding with proximity to the holidays in December.
* Though sales dropped in December, it was still the second highest in the year with 2,568 orders totaling £1,182,625.03 in revenue.
* Other holidays did not reach anywhere near these peaks, with February having the lowest order volume at 1,174 and second lowest earnings at £498,062.65 despite Valentine's Day being a gift-giving holiday.

![image](https://github.com/user-attachments/assets/c9233d9f-ca98-4741-806f-97da756ef955)



### Customer Profile Analysis
* Using Machine Learning algorithms, we were able to analyze customer purchasing behavior to identify the most popular product combinations.
#### Product Support  
* For example, the most popular combination was the Jumbo Bag Pink Polkadot and Jumbo Bag Red being present in 4.1% of all orders.
* Using this we can target product recommendations to facilitate cross-selling; below is a useful heatmap that shows some of the most popular combinations.
* In regards to recommendations provided later, we'll refer to this value as "_Product Support_".

![image](https://github.com/user-attachments/assets/2d5863f4-67db-4145-8337-e465a9c1951d)

  
#### Lift
* Another key insight we uncovered was that certain products had a much higher probability of being bought together, rather than separately.
* These indicate strong relationships between products which can be leveraged through marketing strategies like product bundling.
* The value we're looking at is a ratio, so any number higher than 1 is a sign of a meaningful relationship.
* In regards to recommendations provided later, we'll refer to this value as "_Lift_".

![image](https://github.com/user-attachments/assets/5cf63762-6ebb-4d4b-aa19-8f6427e1fe60)


#### Description Frequency
* Analyzing the text descriptions of purchased products, we noticed some interesting trends with regards to the word 'Christmas'.
* Coinciding with the sharp revenue increase in September, we notice that the presence of the word 'Christmas' in products sold increases by 290% between August and September.
* Also between July and August, the occurrence of the word 'Christmas' increases by 59%.
* This tells us that shoppers seem to start shopping for holiday related items earlier than expected, starting at around August to September.

![image](https://github.com/user-attachments/assets/8203fa2c-9f5d-482f-9d5a-def7e9388604)

### Product Performance
* This company sells a wide assortment of unique products which is reflected by there not being any single product that makes up a majority of the revenue.
* By pure revenue, the Regency Cakestand 3 Tier earned the most with 






