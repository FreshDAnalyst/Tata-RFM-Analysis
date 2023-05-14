# Tata Online Retail Store Analysis

## Introduction
Tata is an online retail store specialized in the sales of different materials.
The CEO and CMO are interested in viewing and understanding how they can use the data to make more meaningful decisions. You would need to provide insights which they can use to create the expansion strategy. The executives want to analyze the trends and the breakdown by different categories so that they have clarity on how the revenue is being generated and what are the main factors affecting the online store.

**Power BI concept applied:**
•	DAX concepts
•	DAX formula to Create Calendar table
•	DAX formula to create RFM analysis

**Problem Statement**
1.	The CEO of the retail store is interested to view the time series of the revenue data for the year 2011 only. He would like to view granular data by looking into revenue for each month. The CEO is interested in viewing the seasonal trends and wants to dig deeper into why these trends occur. This analysis will be helpful for the CEO to forecast for the next year.
2.	The CMO is interested in viewing the top 10 countries which are generating the highest revenue. Additionally, the CMO is also interested in viewing the quantity sold along with the revenue generated. The CMO does not want to have the United Kingdom in this visual.
3.	The CMO of the online retail store wants to view the information on the top 10 customers by revenue. He is interested in a visual that shows the greatest revenue generating customer at the start and gradually declines to the lower revenue generating customers. The CMO wants to target the higher revenue generating customers and ensure that they remain satisfied with their products
4.	The CEO is looking to gain insights on the demand for their products. He wants to look at all countries and see which regions have the greatest demand for their products. Once the CEO gets an idea of the regions that have high demand, he will initiate an expansion strategy which will allow the company to target these areas and generate more business from these regions. He wants to view the entire data on a single view without the need to scroll or hover over the data points to identify the demand. There is no need to show data for the United Kingdom as the CEO is more interested in viewing the countries that have expansion opportunities.

**Data Sourcing**

The data is from online Forage internship program. I then downloaded the CSV file extract it into power BI for cleaning, modelling analysis and visualization.
It contains eight(8) columns with 541910 rows of data.
The columns includes: **InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID & Country**

**Data Transformation/Cleaning:**
Data was efficiently cleaned and transformed with the Power Query Editor of Power BI. [a screenshot of the applied steps] some of the applied steps included.
•	Changed the **InvoiveNo, CustomerID and StockCode** Column from number to text datatype
•	Split the values in the **InvoiceDate** column which contain the date and time and rename the new column containing the time as **Time**
•	Filtered out values in the **Quantity** column that are below 1
•	Filtered out values in the **UnitPrice** column that are negative or below $0
•	Filtered out null values

**Data Modelling**

The data is a single table dataset
•	I Created a calendar table containing 2010 – 2011 dates

## Answers

The following are answers to the business question. Gotten from the analysis and visualization
1.	To view the time series of the revenue data for the year 2011 only, I first created a DAX formula to create a column to calculate the total amount for each sales.      _image below_

![](https://github.com/FreshDAnalyst/Tata-RFM-Analysis/blob/main/Formular%20for%20total.PNG) 

Then I created a DAX formula to calculate the Total revenue.   _Image below.._

![](https://github.com/FreshDAnalyst/Tata-RFM-Analysis/blob/main/Formular%20for%20Revenue.PNG)

The visuals shows February and April 2011 has the lowest overall sales while revenue start to raise to the peak from August to November. Where November is the peak month of revenue and then revenue drops by december.   _Image below_

![](https://github.com/FreshDAnalyst/Tata-RFM-Analysis/blob/main/Question%201%20chart.PNG)

2.	To view the top 10 countries which are generating the highest revenue and also the quantity sold along with the revenue generated without showing that United Kingdom is the visuals.
I first created a measure with DAX to calculate the total quantity.    _Image below._

![](https://github.com/FreshDAnalyst/Tata-RFM-Analysis/blob/main/Formular%20for%20Total%20quantity.PNG)

The top 10 countries which are generating the highest revenue and quantity sold without the United Kingdom are below with Netherland and EIRE(Ireland) as the top 2 highest.  _Image below_

![](https://github.com/FreshDAnalyst/Tata-RFM-Analysis/blob/main/Question%202%20visuals.PNG)

Checking deeper into the insight shows customers in Sweden buys less expensive products in high quantity while customers in Spain and Belgium buys more expensive products in lower quantity

3.	To view the top 10 customers by revenue down to the lowest revenue generating customers. _Image below_

![](https://github.com/FreshDAnalyst/Tata-RFM-Analysis/blob/main/Question%203%20visual.PNG)

The visual shows that the customer with the highest revenue is customerID 14646. 

4.	To view at all countries and see which regions have the greatest demand for their products apart from the United Kingdom.    _Image below_

![](https://github.com/FreshDAnalyst/Tata-RFM-Analysis/blob/main/Question%204%20visual.PNG)

It shows Netherland, Ireland, Germany and France are the countries with the greatest demand for the products apart from the United Kingdom. Meaning the CEO can initiate an expansion Strategy in those countries to generate more revenue and business growth

# RFM Analysis

RFM analysis is a customer segmentation technique used in marketing to identify and target specific groups of customers based on their purchasing behavior. The acronym "RFM" stands for:
RECENCY: How recently a customer has made a purchase
FREQUENCY: How often a customer makes purchases
MONEARY VALUE: How much a customer spends on purchases
RFM analysis involves analyzing these three customer behaviors and segmenting customers into different groups based on their scores for each behavior.

**Creation of RFM Measures**
I first created some calculated measures with DAX for the Last Transaction date, Recency, Frequency and Monetary Value measures. 
**Recency** refers to the time elapsed since a customer's last transaction.Customers who have recently made a purchase are considered more valuable than those who haven't made a purchase in a while.
**Frequency** refers to the number of purchases a customer has made. Customers who make frequent purchases are considered more valuable than those who make infrequent purchases.
**Monetary value** refers to the amount of money a customer has spent on purchases. Customers who have spent more money are considered more valuable than those who have spent less money            _image below_

**RECENCY**

![](https://github.com/FreshDAnalyst/Tata-RFM-Analysis/blob/main/Recency%20DAX.PNG)

**FREQUENCY**

![](https://github.com/FreshDAnalyst/Tata-RFM-Analysis/blob/main/Frequency%20DAX.PNG)

**Monetary Value**

![](https://github.com/FreshDAnalyst/Tata-RFM-Analysis/blob/main/Monetary%20DAX.PNG)

**Creation of RFM table**

•	Then I created the RFM table using DAX formula which consist of columns that shows the Recency, Frequency and Monetary value of each customers  _image below_

![](https://github.com/FreshDAnalyst/Tata-RFM-Analysis/blob/main/RFM%20table%20DAX%20formula.PNG)

and then another DAX formula was used to create scores into four(4) percentiles (5,4,3,2or1) respectively, (5 which indicate as highest score and 1 or 2 indicates as lowest score).  DAX formular  _image below…_

![]()










