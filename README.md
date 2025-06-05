# Customer Segmentation & Order Cancellation Analysis
This project deals with Customer Segmentation based on purchasing power and Order Cancellation analysis of Sales data. The implementation is done using Python.

## Dataset used
Amazon Fashion retail data (from Kaggle): 128k records, 23 fields

## Motivation
1. Customer Segmentation helps target the right products to the right customers, increasing conversion rates. It also helps with understanding which customer segments prefer which products helps avoid overstocking or stockouts.
2. Order cancellation analysis is important because frequent cancellations could indicate supply chain or listing issues. High cancellation rates can also damage seller metrics and visibility on Amazon.

## Concepts covered
1. K-means
2. Principle Component Analysis (PCA)
3. Logistic Regression

## Customer Segmentation
1. Data pre-processing
2. Used PCA for dimensionality reduction.
3. Used K-means with k=3.
4. Analysed the obtained clusters to find patterns that can help with marketing products to these specific clusters.

### Graph generated after PCA & K-means
![K-means Graph](/kmeans_graph.png)

### Cluster Analysis
<img src="/category_analysis.png" alt="Category-wise analysis" height="150"/>
<img src="/cluster_analysis.png" alt="Cluster analysis" height="150"/>

**Cluster 0 (Budget Shoppers):** This cluster has low-spend shoppers who tend to have single-item purchases. The purchases are dominated by the ‘Kurta’ category (57%). <br>
**Cluster 1 (Premium Shoppers):** This cluster has high-value shoppers but still single-item purchases. The purchases are dominated by the ‘Set’ category (62%). <br>
**Cluster 2 (High-end multi-item Shoppers):** This cluster has the highest spenders with multi-item purchases. The purchases are dominated by the ‘Kurta’ (47%) and ‘Set’ (30%) categories.


## Order Cancellation Analysis
### Exploratory analysis of the data <br>
   <img src="/cancelation_by_state.png" alt="Cancelation Rate by State" width="300"/>
   <img src="/amount_by_cancelation_status.png" alt="Avg. Amount by Cancelation status" width="300"/>
   <img src="/cancelation_by_category.png" alt="Cancelation Rate by Category" width="300"/>
  <img src="/cancelation_by_fulfillment_method.png" alt="Cancelation Rate by Fulfillment Method" height="300"/>
  <img src="/cancelation_by_promotion.png" alt="Cancelation Rate by Promotion Presence" width="300"/>
### Correlation analysis
It can be seen from the above data that:
1. Cancellation Rate is significantly higher in items which do not have promotion.
2. Cancellation Rate is slightly higher for orders from an external Merchant.

5. Used Logistic regression for Predictive analysis.

