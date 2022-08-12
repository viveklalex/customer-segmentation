
# Customer Segementation using RFM 
[![MIT License](https://img.shields.io/apm/l/atomic-design-ui.svg?)](https://github.com/tterb/atomic-design-ui/blob/master/LICENSEs)

Customer Segementation using RFM analysis.
## Introduction 

 
![alt text](https://raw.githubusercontent.com/viveklalex/customer-segmentation/master/images/intro_.jpg) 

      
#### What is Segment Customers?

Customer segmentation is the process of dividing customers into groups based on common characteristics so companies can market to each group effectively and appropriately.

#### Why Segment Customers?

Segmentation allows marketers to better tailor their marketing efforts to various audience subsets. Those efforts can relate to both communications and product development. Specifically, segmentation helps a company:

Create and communicate targeted marketing messages that will resonate with specific groups of customers, but not with others (who will receive messages tailored to their needs and interests, instead).

1)Select the best communication channel for the segment, which might be email, social media posts, radio advertising, or another approach, depending on the segment.

2)Identify ways to improve products or new product or service opportunities.

3)Establish better customer relationships.

4)Test pricing options.

5)Focus on the most profitable customers.

6)Improve customer service.

7)Upsell and cross-sell other products and services.

#### What is RFM Analysis?

RFM analysis allows marketers to target specific clusters of customers with communications that are much more relevant for their particular behavior – and thus generate much higher rates of response, plus increased loyalty and customer lifetime value. Like other segmentation methods, an RFM model is a powerful way to identify groups of customers for special treatment. RFM stands for recency, frequency and monetary – more about each of these shortly.

Marketers typically have extensive data on their existing customers – such as purchase history, browsing history, prior campaign response patterns and demographics – that can be used to identify specific groups of customers that can be addressed with offers very relevant to each.

RFM factors illustrate these facts:

1)the more recent the purchase, the more responsive the customer is to promotions

2)the more frequently the customer buys, the more engaged and satisfied they are

3)monetary value differentiates heavy spenders from low-value purchasers

#### What are Recency, Frequency and Monetary?

Underlying the RFM segmentation technique is the idea that marketers can gain an extensive understanding of their customers by analyzing three quantifiable factors. These are:

**Recency** : How much time has elapsed since a customer’s last activity or transaction with the brand? Activity is usually a purchase, although variations are sometimes used, e.g., the last visit to a website or use of a mobile app. In most cases, the more recently a customer has interacted or transacted with a brand, the more likely that customer will be responsive to communications from the brand.

**Frequency**: How often has a customer transacted or interacted with the brand during a particular period of time? Clearly, customers with frequent activities are more engaged, and probably more loyal, than customers who rarely do so. And one-time-only customers are in a class of their own.

**Monetary**: Also referred to as “monetary value,” this factor reflects how much a customer has spent with the brand during a particular period of time. Big spenders should usually be treated differently than customers who spend little. Looking at monetary divided by frequency indicates the average purchase amount – an important secondary factor to consider when segmenting customers.

Based on RFM value we categorize customers into 3 groups

**Low Value**: Customers who are less active than others, not very frequent buyer/visitor and generates very low - zero - maybe negative revenue.

**Mid Value**: In the middle of everything. Often using our platform (but not as much as our High Values), fairly frequent and generates moderate revenue.

**High Value**: The group we don’t want to lose. High Revenue, Frequency and low Inactivity.


          
## Overview 
- Datasets and Data-Loading
- Data Preprocessing
- Exploratory Data Analysis:
- Model creation and training

### Datasets and Data-Loading

Dataset is collected from  https://www.kaggle.com/datasets/vijayuv/onlineretail

The dataset consists of 541909 examples and  8 columns.

Columns :

![alt text](https://raw.githubusercontent.com/viveklalex/customer-segmentation/master/images/columns.png)


### Data Preprocessing

We haven't done any preprocessing.

### Exploratory Data Analysis:

Exploratory Data Analysis using Pandas and visualized using Matploilib

### Model building and training

Customer Segementation has two steps:

1)
RFM Calculation:
  - **Customer ID / Email / Name etc**: to identify them
- **Recency (R)** as days since last purchase: How many days ago was their last purchase? Deduct most recent purchase date from today to calculate the recency value. 1 day ago? 14 days ago? 500 days ago?
- **Frequency (F)** as total number of transactions: How many times has the customer purchased from our store? For example, if someone placed 10 orders over a period of time, their frequency is 10.
- **Monetary (M)** as total money spent: How many $$ (or whatever is your currency of calculation) has this customer spent? Again limit to last two years – or take all time. Simply total up the money from all transactions to get the M value.


2)

KMeans Clustering 
K-Means Clustering is an Unsupervised Learning algorithm, which groups the unlabeled dataset into different clusters.
We group the Recency, Frequency, Monetary into four groups selected by Elbow method.

## Results

 Recency Cluster

![alt text](https://raw.githubusercontent.com/viveklalex/customer-segmentation/master/images/rescency_cluster.png)

Frequency Cluster

![alt text](https://raw.githubusercontent.com/viveklalex/customer-segmentation/master/images/Frequency_cluster.png) 

Revenue Cluster

![alt text](https://raw.githubusercontent.com/viveklalex/customer-segmentation/master/images/revenue_cluster.png) 

Overall Scoring

![alt text](https://raw.githubusercontent.com/viveklalex/customer-segmentation/master/images/overall_mean.png)


Segemented Customers

![alt text](https://raw.githubusercontent.com/viveklalex/customer-segmentation/master/images/seg_cust.png)

## Contributing

Contributions are always welcome!
