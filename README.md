# **Project Background**

This transactional data set contains all transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered online retail store. The company mainly sells unique all-occasion gifts, and many of its customers are wholesalers.

Insights and recommendations are provided on the following key areas:
* Insights on customers established from behavioral segmentation, based on the overall monetary value, recency, and frequency of purchases by customers.
* Insights on behavioral patterns of outlier customers compared to non-outlier customers.
* Marketing and customer retention plans tailored to customer clusters based on economic behavior.
* Reactivation campaigns for inactive customers.
* Loyalty and reward campaigns for loyal and high-value customers.

The notebook used to inspect and clean the data for this analysis can be found here [link](https://github.com/Just-Aymz/RFM-Segmentation-Analysis/blob/main/Preprocessing.ipynb).

# **Data Structure & Initial Checks**

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

# **Executive Summary** 
### **Overview of Findings**:

A total of nine distinct customer clusters have been identified, which can be grouped into two primary behavioral segments: non-outlier and outlier customers based on the features of Monetary Value, Recency, and Frequency.

For the non-outlier segment, the median Monetary Value is approximately £600.00 to £650.00, with a purchase Frequency of 2 and a median Recency of 52 days between transactions. In contrast, customers in the outlier segment demonstrate significantly higher engagement, with a median Monetary Value of around £5180.00, a Frequency of 13 purchases, and a Recency of just 11 days between transactions.

This segmentation allows for a refined understanding of customer behaviors, supporting more targeted engagement strategies.

![output](https://github.com/user-attachments/assets/6cfbd065-7e58-4b91-9ad8-579339009be9)

# **Insights Deep Dive**
1. **Non-Outlier Category**:
   * Customers in the non-outlier category are predominantly newer clients. Clusters in this category demonstrate a lower Monetary Value relative to those in the outlier category, indicating their early-stage engagement with our organization.
   * The clusters providing the highest Monetary Value include *New High-Value, Engaged Customer (0)*, and *High-Value, Interested Customer (1)* groups.
   * The cluster with the highest median Recency value identifies *Once-Off Customers (3)*, as evidenced by a median Frequency of 1.

![output](https://github.com/user-attachments/assets/66439754-6d80-4c33-a795-29c0ccd1812b)

2. **Outlier Category**:
   * Customers in the outlier category are predominantly our most frquent customers. Clusters in this category demonstrate a high monetary value.
   * The clusters providing the highest Monetary Value include: *Lapsed Customers (4)*, and *Active, High-value Customer (5)*.

![output](https://github.com/user-attachments/assets/d0167b3b-4c39-46dd-9b15-23f0366791bf)
 # **Recommendations**

 ### 1. **Non-Outlier Category**:
   * *New High-Value, Engaged Customer* (Cluster 0):
      * **Recommendation**: Develop personalized loyalty programs or exclusive benefits to encourage further engagement and repeat purchases. Since these customers have a high spending rate and frequent purchases, timely promotions or membership tiers could reinforce their commitment.
    * *New Customer* (Cluster 1):
      * **Recommendation**: Focus on nurturing these new customers through targeted onboarding campaigns and personalized follow-ups. Offering discounts on subsequent purchases or exclusive recommendations may improve retention and transition these customers to more engaged segments.
    * *High-Value, Interested Customer* (Cluster 2):
      * **Recommendation**: Provide tailored upsell or cross-sell offers, as these customers show consistent spending and frequency. A targeted strategy with exclusive previews or bundled offers could maximize their value, converting them into loyal, high-value customers.
    * *Once-Off Customer* (Cluster 3):
      * **Recommendation**: Implement targeted win-back campaigns, such as reminder emails or limited-time discounts. For customers in this category, re-engagement strategies like seasonal offers or incentives for a second purchase may encourage repeat business.
   
### 2. **Outlier Category**:
  * *Lapsed Customer* (Cluster 4):
      * **Recommendation**: To reactivate these high-value but lapsed customers, offer a re-engagement incentive like a time-sensitive discount or exclusive event invitation. Highlighting past high-value purchases with personalized communications could rekindle interest.
  * *Active, High-Value Customer* (Cluster 5):
      * **Recommendation**: Reinforce loyalty by recognizing their high engagement and value. Offer VIP services or early access to new products. Implementing a customer rewards system could encourage these valuable customers to maintain or increase their purchase frequency.  
  * *Active, Moderate-Value Customer* (Cluster 6):
      * **Recommendation**: Focus on increasing their spending through upselling and cross-selling. Offer these customers bundles, tiered discounts, or loyalty programs that reward higher spend thresholds to elevate their engagement and value further.
  * *Disengaged Customer* (Cluster 7):
      * **Recommendation**: Use re-engagement campaigns focusing on the unique benefits of continued patronage. Highlight recent products and include limited-time offers to incentivize re-engagement. Consider surveying this segment to better understand potential barriers to frequent purchases.
  * *Lapsed Once-Off Customer* (Cluster 8):
      * **Recommendation**: Since this group has minimal recent engagement and spending, focus on low-cost re-engagement strategies, such as periodic, automated email reminders. Consider seasonal promotions or special offers that are likely to catch their attention and encourage a re-purchase.

### 3. **General Recommendations**:
  * **Data-Driven Personalization**: Use cluster insights to personalize communications and target marketing strategies according to each segment’s unique behaviors and spending habits.
  * **Customer Feedback and Insight Collection**: Survey or gather feedback from lapsed and disengaged clusters (e.g., Lapsed Customers, Disengaged Customers) to understand potential pain points and address factors that might improve their satisfaction and engagement.
