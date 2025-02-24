# Project Background
This project will be using the transactional data for a UK e-commerce retail site. The company mainly sells unique all-occasion gifts with customers primarily being wholesalers.

We will throughly analyze and synthesize the data provided to uncover critical insights and provide valuable recommendations to increase their commercial success.

Insights and recommendations will be provided in the following areas: 
* Sales Trends Analysis: Evaluation of sales patterns with a focus on Revenue, Order Volume, and Seasonal Trends.
* Customer Profile Analysis: Analysis of customer purchasing behavior to better understand what products were bought together most frequently and what product descriptors interested customers the most.
* Inventory Management: Providing recommendations on when to start stocking certain seasonal items along with recommendations on the prioritization of certain items.
  
An interactive Tableau Dashboard can be found [here](https://public.tableau.com/shared/6FN5TPWRW?:display_count=n&:origin=viz_share_link).

The Python code used to clean and transform the data can be found in the following notebook [here](ECommerce_UK_Cleaning.ipynb).

The Python code used to analyze the data with ML Functions can be found in the following notebook [here](Ecommerce_uk_MLFunctions.ipynb).

### Basic Overview of the Data

The unaltered data can be downloaded [here](ecommerceUK_RAW.rar).

The cleaned and transformed data can be downloaded [here](ecommerceUK_CLEANED.rar).

The unaltered data consists of 8 columns: InvoiceNo, StockCode, Description, InvoiceDate, Quantity, UnitPrice, CustomerID, and Country. It has a total row count of 541,910 rows.

The transformed data separates the InvoiceDate into Month, Day of the Week, and Time of Purchase. It also adds a column for totals by multiplying Quantity and Unit price. It has a total row count of 530,693 rows.

The transformed data consists of 11 columns: InvoiceNo, StockCode, Description, Quantity, UnitPrice, CustomerID, Country, Year, Day, Time, and Totals. 

# Executive Summary

### Overview of Findings 
Unsurprisingly, the company's peak revenue was achieved during the latter half of the year, approaching Christmas. Surprisingly though, this increase in revenue starts in September which experiences a 33% boost in revenue and a 25% increase in order volume compared to August. Though this is the largest percentwise change between months; overall revenue and order volume peaks in November with a 26% increase in revenue and a 23% increase in order volume compared to October. We'll explore below on how we can further capitalize on this trend using customer purchasing behavior displayed during this time.


### Sales Trends
* The company achieved an overall revenue of £9,747,747.93 in this timeframe with 22,061 orders. 
* Company sales peaked in November with 3,021 orders totaling £1,461,756.25 in monthly revenue, corresponding with proximity to the holidays in December.
* Though sales dropped in December, it was still the second highest in the year with 2,568 orders totaling £1,182,625.03 in revenue.
* Other holidays did not reach anywhere near these peaks, with February having the lowest order volume at 1,174 and second lowest earnings at £498,062.65 despite Valentine's Day being a gift-giving holiday.

![image](https://github.com/user-attachments/assets/c9233d9f-ca98-4741-806f-97da756ef955)



### Customer Profile Analysis
Using Machine Learning algorithms, we were able to analyze customer purchasing behavior to identify the most popular product combinations. Here are the insights we gained from that:
  
#### Product Support  
* This is the probability of customers buying a certain combination of products in an order. For example the most popular combination was the Jumbo Bag Pink Polkadot and Jumbo Bag Red, being present in 4.1% of all orders.
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
* Analyzing the text descriptions of purchased products, we noticed some interesting trends. One we'll explore in detail is the word 'Christmas'.
* Coinciding with the sharp revenue increase in September, we notice that the presence of the word 'Christmas' in products sold increases by 290% between August and September.
* Such a large increase implies that customers seem to start shopping for holiday related items earlier than expected, starting at around late August to September.
  
![image](https://github.com/user-attachments/assets/8203fa2c-9f5d-482f-9d5a-def7e9388604)


### Recommendations:

With the insights that we've unearthed, we recommend the following:
* September experienced the largest increase in revenue (33%) and order volume (25%), capitalizing on that sudden sales boost should be high-priority. **Starting promotional campaigns towards the end of August and early September would provide the sudden wave of customers, who are already eager to purchase, incentive to purchase more.**

* For orders placed, the presence of the word "christmas" increased by 290% in September with almost every subsequent month continuing this trend. Similarly, other product descriptors like "red", "vintage", and "heart" also experienced high interest from customers. **Doing something as simple as re-branding merchandise to have "Christmas" or another popular descriptor in its description would be a great way to boost customer sentiment without much effort.**

* Order volume continually increases almost every month after August with November reaching a peak that exceeds August's volume by over 100%. **It is advisable re-evaluate inventory and stock up on holiday related items as early as August to ensure that such order volumes can be met.**

* _Product Support_ shows that we have multiple product combinations that appear together relatively frequently in orders. For example, the Alarm Clock BakeLike Green and the Alarm Clock BakeLike Red products are present together in 3.2% of all orders but (looking at the confidence value) it's only 65% likely that someone buying the former also buys the latter. **We recommend using this to generate product recommendations, giving the 35% of people who only bought the former product the idea to buy the latter provides a great cross-selling opportunities.**

* _Lift_ shows that there are product combinations that are bought together far more frequently than they are separately. **This provides a unique opportunity where promotional strategies such as bundling could be useful. If customers are already looking to buy two separate products together, then upselling them by offering those products bundled with a third related product could be effective.**
