# Data Analysis on Fashion Industry
## Optimizing Fashion Store Strategies: K-means Clustering of Sales and Profit

## Table of Contents

- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Data Analysis](#data-analysis)
- [Machine Learning Application](#machine-learning-application)
- [Results](#results)
- [Recommendations](#recommendations)
- [References](#references)
- [Contacts](#contacts)

### Project Overview
This research project leverages publicly available datasets and synthetic data to explore opportunities for enhancing business operations in the fashion retail sector. Drawing from a familial background deeply rooted in the fashion industry, the project employs methodologies such as K-means clustering to extract actionable insights. By meticulously analyzing these data points, the goal is to uncover areas of improvement and potential inefficiencies. Through this project, we aim to demonstrate the power of data-driven decision-making in shaping strategies within the fashion retail landscape.

### Data Source

Fashion Sales Data: The primary dataset used for this analysis is the "Adidas US Sales Datases.xlsx" file, containing detailed information about each sales made by different retail store in different region.

### Tools

- Excel                        : Data Cleaning
- SQL Server Management Studio : Data Analysis
- Python                       : Data preprocessing, machine learning application, data visualization


### Data Cleaning/Preparation

In the initial data preparation phase, we performed the following tasks:
1. Data loading.
2. Data cleaning and formatting.

### Data Analysis

Data analysis using SQL to find insights using SQL code, such as:

```sql
SELECT DISTINCT([City]), SUM([Units Sold]), SUM([Operating Profit]) 
FROM ['Adidas US Sales$']
GROUP BY City
```

### Data Preprocessing

Preparing data for next steps with pandas library, such as:
1. Scaling dataset with min-max scaler with interesting code:
   ```python
   df[] = ((df[] - df[].min())/(df[].max() - df[].min())) * 9 + 1
   ```
2. Specifying data to use dataset in year 2020 and specific product only.

### Machine Learning Application

Using KMeans algorithm from sklearn library to cluster data with these steps:
1. Determined how many cluster to use by using elbow method
2. Fitting dataset into KMeans algorithm with these code:
   ```python
   km = KMeans(n_clusters=4)
   km.fit(df[[X,Y]])
   ```
   ![Elbow point](https://github.com/santaa7/David-s_Portofolio/assets/98442051/708ae050-83ae-4eeb-b0f8-54999b7e9edf)

3. Fitting the result into new column in that dataset.
4. Plot the result with pyplot :

   ![Cluster Plot](https://github.com/santaa7/David-s_Portofolio/assets/98442051/eb141565-5905-4752-9f1a-694163c85752)

### Results

The analysis results are summarized as follows:
1. The result contain 4 cluster of sales performance by each invoice issued in 2020 and only contain Men's apparel. Sales performance can be seen from units sold and operating profit.
2. Cluster 0 (Purple) have an average units sold of 91 and an average operating profit of $3652. Cluster 1 (Blue) have an average units sold of 700 and an average operating profit of $174419. Cluster 2 (Green) have an average units sold of 465 and an average operating profit of $96026. Cluster 3 (Yellow) have an average units sold of 233 and an average operating profit of $33744.   
3. Cluster 0 dominates the entire point with 995 data point. This indicate most sales has few unit sold and low operating profit. 
4. The highest average in units sold and operating profit presented as cluster 1, only have 67 data point. This indicate only 67 sales in Men's apparel product clustered as high performance sales.
5. From the dataset in cluster 0 (low performance), none of which are in New York city. And from cluster 1 (high performance), 13 sales data are from New York city.

### Recommendations

Based on the analysis, we recommend the following actions :
- Improve sales in low sales performance area by increasing advertising in each of low sales performance store.
- Applying strategies thats applied in high sales performance store to low sales performance store.
- Do a consumer analysis to better understand the market in low sales performance area.

### References

1. KMeans Clustering Algorithm by Turner Luke
2. [Stack Overflow](https://stackoverflow.com/)

### Contacts

- LinkedIn - www.linkedin.com/in/davidaquinaldo
- Email - davidaquinaldo@gmail.com

