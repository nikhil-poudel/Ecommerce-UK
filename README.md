# Project Background
This project will be using the transactional data for a UK e-commerce retail site. The company mainly sells unique all-occasion gifts with many customers being wholesalers.

We will throughly analyze and synthesize the data provided to uncover critical insights and provide valuable recommendations to increase their commercial success.

Insights and recommendations will be provided in the following areas: 
* Sales Trends Analysis: Evaluation of sales patterns with a focus on Revenue, Order Volume, and Seasonal Trends.
* Inventory Management Analysis: Providing recommendations on when to start stocking certain seasonal items along with recommendations on the prioritization of certain items.
* Customer Profile Analysis: Analysis of customer purchasing behavior to better understand what products were bought together most frequently and what product descriptors interested customers the most.
* Product Performance: Evaluation of product performance throughout the year and in different regions.

An interactive Tableau Dashboard can be found [HERE].
The Python code used to clean, analyze, and transform the data can be found [HERE].

# Basic Overview of the Data
The uncleaned and unaltered data can be found [HERE].

The cleaned and transformed data can be found [HERE].

The unaltered data consists of 8 columns: InvoiceNo, StockCode, Description, InvoiceDate, Quantity, UnitPrice, CustomerID, and Country.

The transformed data separates the InvoiceDate into Month, Day of the Week, and Time of Purchase. It also adds a column for totals by multiplying Quantity and Unit price.

The transformed data consists of 11 columns: InvoiceNo, StockCode, Description, Quantity, UnitPrice, CustomerID, Country, Year, Day, Time, and Totals. 

