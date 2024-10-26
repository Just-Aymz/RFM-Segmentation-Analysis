# Project Background

This transactional data set contains all transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered online retail store. The company mainly sells unique all-occasion gifts, and many of its customers are wholesalers.

Insights and recommendations are provided on the following key areas:
* Insights on customers established from behavioral segmentation, based on the overall monetary value, recency, and frequency of purchases by customers.
* Insights on behavioral patterns of outlier customers compared to non-outlier customers.
* Marketing and customer retention plans tailored to customer clusters based on economic behavior.
* Reactivation campaigns for inactive customers.
* Loyalty and reward campaigns for loyal and high-value customers.

The notebook used to inspect and clean the data for this analysis can be found here [link]().

The notebook regarding clustering and various business questions and visualization can be found here [link]().

An interactive Power BI dashboard used to report and explore sales trends can be found here [link]().

# Data Structure & Initial Checks

The datacard for this dataset can be found at: [Link](https://archive.ics.uci.edu/dataset/352/online+retail). An overview is provided below. 

| Variable Name | Role | Type | Description | Units | Missing Values |
| ------------- | ---- | ---- | ----------- | ----- | -------------- |
| InvoiceNo | ID | Categorical | A 6-digit integral number uniquely assigned to each transaction. If this code starts with the letter 'c', it indicates a cancellation | - | No |
| StockCode | ID | Categorical | A 5-digit integral number uniquely assigned to each distinct product | - | No |
| Description | Feature | Categorical | Product Name | - | No |
| Quantity | Feature | Integer | The quantities of each product (item) per transaction | - | No |
| InvoiceDate | Feature | Date | The day and time when each transaction was generated | - | No |
| UnitPrice | Feature | Continuous | Product price per unit | Sterling | No |
| CustomerID | Feature | Categorical | a 5-digit integral number uniquely assigned to each customer | - | No | 
| Country | Feature | Categorical | The name of the country where each customer resides | - | No |

# Executive Summary 
### **Overview of Findings**:

A total of nine distinct customer clusters have been identified, which can be grouped into two primary behavioral segments: non-outlier and outlier customers based on the features of Monetary Value, Recency, and Frequency.

For the non-outlier segment, the median Monetary Value is approximately £600.00 to £650.00, with a purchase Frequency of 2 and a median Recency of 52 days between transactions. In contrast, customers in the outlier segment demonstrate significantly higher engagement, with a median Monetary Value of around £5180.00, a Frequency of 13 purchases, and a Recency of just 11 days between transactions.

This segmentation allows for a refined understanding of customer behaviors, supporting more targeted engagement strategies.

![output](https://github.com/user-attachments/assets/6cfbd065-7e58-4b91-9ad8-579339009be9)

# Insights Deep Dive
