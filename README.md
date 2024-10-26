# Project Background

This transactional data set contains all transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered online retail store. The company mainly sells unique all-occasion gifts, and many of its customers are wholesalers.

Insights and recommendations are provided on the following key areas:
* Insights on customers established from behavioral segmentation, based on the overall monetary value, recency, and frequency of purchases by customers.
* Insights on behavioral patterns of outlier customers compared to non-outlier customers.
* Marketing and customer retention plans tailored to customer clusters based on economic behavior.
* Reactivation campaigns for inactive customers.
* Loyalty and reward campaigns for loyal and high-value customers.

The notebook used to inspect and clean the data for this analysis can be found here [link](https://github.com/Just-Aymz/RFM-Segmentation-Analysis/blob/main/Preprocessing.ipynb).

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
1. **Non-Outlier Category**:
   * Customers in the non-outlier category are predominantly newer clients. Clusters in this category demonstrate a lower Monetary Value relative to those in the outlier category, indicating their early-stage engagement with our organization.
   * The clusters providing the highest Monetary Value include *New High-Value, Engaged Customer (0)*, and *High-Value, Interested Customer (1)* groups.
   * The cluster with the highest median Recency value identifies *Once-Off Customers (3)*, as evidenced by a median Frequency of 1.

![output](https://github.com/user-attachments/assets/66439754-6d80-4c33-a795-29c0ccd1812b)

2. **Outlier Category**:
   * Customers in the outlier category are predominantly our most frquent customers. Clusters in this category demonstrate a high monetary value.
   * The clusters providing the highest Monetary Value include: *Lapsed Customers (4)*, and *Active, High-value Customer (5)*.

![output](https://github.com/user-attachments/assets/d0167b3b-4c39-46dd-9b15-23f0366791bf)


