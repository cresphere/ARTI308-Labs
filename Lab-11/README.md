# Lab 10
In this lab the required code for the second file has been filled in.

---

## Final Questions

Answer the following questions:

1. Why is this an unsupervised learning problem?  
Because the data is unlabeled, the model will only find patterns

2. Why did we remove the `CUST_ID` column?  
It does not provide useful data for the machine learning model and adding it would add noise

3. Which columns had missing values?  
Minimum payments and Credit limit

4. How did you handle the missing values?  
Mean imputation

5. Why is scaling important before applying K-Means?  
Because one feature may have numbers between 0 and 9999 while another feature may have between 1 and 10, the feature with larger values will dominate and the model will be inaccurate if not scaled

6. Which K value did you choose? Explain your answer using the elbow method and silhouette score.  
K=3 because the elbow graph has a clear bend at 3, whilst the silhoutte score peaked at 3

7. Based on the cluster summary table, describe each customer segment in your own words.  
Cluster 1: Customer with high spending and activity
Cluster 0: Customers with a medium amount of spending (the average customer)
Cluster 2: Customers with low spending

8. Which cluster may represent high-value customers?  
Cluster 1

9. Which cluster may represent customers who rely more on cash advance?  
Cluster 2, since they have a lower purchase activity

10. How can a company use these clusters for marketing strategy?  
Offer varying amounts of increased points rewards, and increased limits based on each cluster, for cluster 2 specifically, use targeted marketing to promote benefits of using a credit card.