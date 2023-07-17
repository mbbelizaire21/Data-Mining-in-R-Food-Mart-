# Data-Mining-in-R-Food-Mart-
Discovering patterns within data to help build insights with Association Rule Mining, Decision Trees, and K-Means Clustering algorithms.

# Overview
This project focuses on the analysis of retail data to gain insights into various aspects of sales, customer behavior, and media promotion. The project involves data cleaning, visualization, association rule mining, clustering, and decision tree modeling. The data used in this project is stored in a CSV file named "media prediction and its cost.csv." that was acquired from Kaggle.com

# Data Cleanse and Preprocessing
The "media prediction and its cost.csv" file is loaded into the R environment as a data frame named retail.

Unnecessary columns that do not contribute to the analysis are removed.

Data is filtered to include only records from the USA sales country.

<img width="887" alt="image" src="https://github.com/mbbelizaire21/Data-Mining-in-R-Food-Mart-/assets/125572462/36e0a37c-4494-41e4-9198-9abc92a74ce3">

# Data Visualization
Various graphs are generated to visualize different aspects of the retail data:

Relationship between the store sales and costs. The more spent at stores, the more sales the stores will receive
<img width="345" alt="image" src="https://github.com/mbbelizaire21/Data-Mining-in-R-Food-Mart-/assets/125572462/f0c56b88-e123-4d44-bbb6-66c24fb930b5">

Unit Sales By Food Department

<img width="324" alt="image" src="https://github.com/mbbelizaire21/Data-Mining-in-R-Food-Mart-/assets/125572462/86083faf-7af0-4837-93c6-47eff6a580d1">

Occupation By Membership Card

<img width="318" alt="image" src="https://github.com/mbbelizaire21/Data-Mining-in-R-Food-Mart-/assets/125572462/b849df4d-bc3b-4ed5-854d-5ba467130d58">

Average Income By Gender

<img width="319" alt="image" src="https://github.com/mbbelizaire21/Data-Mining-in-R-Food-Mart-/assets/125572462/5b1cb56f-30ab-4056-adb8-1445a5364127">

# Association Model
The arules and arulesViz libraries are used to perform association rule mining on the retail data.
Frequent itemsets and association rules are generated using the apriori function with different support and confidence thresholds.

Association rules are created by searching data for frequent if-then patterns and using the criteria support and confidence to identify the most important relationships.

•	Support – an indication of how frequently the items appear in the data.

•	Confidence – the number of times the if-then statements are found true.

•	Lift – A third metric which can be used to compare confidence with expected confidence, or how many times an if-then statement is expected to be found true

In applying the Association Rule Mining method to this project, the outcome is set as RHS (or Right Hand Side) to see how other factors might affect to the outcome.

Support = 0.11 and Confidence = 0.8 creates 32 rules which is sufficient for analysis

<img width="382" alt="image" src="https://github.com/mbbelizaire21/Data-Mining-in-R-Food-Mart-/assets/125572462/5d54a25b-ac92-4767-8cb4-d8413b3ddb3c">


# Decision Tree

Decision tree method is a commonly used data mining method for establishing classification systems based on multiple covariates or for developing prediction algorithms for a target variable. A decision tree model is built to predict the 'media_type' based on the 'cost' variable using the rpart package. The model is trained on a subset of the data and evaluated on the test data.

<img width="365" alt="image" src="https://github.com/mbbelizaire21/Data-Mining-in-R-Food-Mart-/assets/125572462/bf5cd8cd-2cfd-42c1-a459-1442af76b3d1">
<img width="331" alt="image" src="https://github.com/mbbelizaire21/Data-Mining-in-R-Food-Mart-/assets/125572462/ea040262-1866-40d0-96e5-47eeadc951cb">

# Clustering
K-Means clustering is applied to cluster the data based on the 'media_type' and 'cost' variables.
Hierarchical Agglomerative Clustering (HAC) is used to visualize clustering results with different distance metrics.
Decision Tree Model

One of the most common exploratory data analysis techniques is clustering. And, one of the most used clustering algorithms due to its simplicity is K-means. This algorithm tries to partition the dataset into K pre-defined distinct non-overlapping subgroups (or clusters) where each data point belongs to only one group.

•	K: Number of clusters

K = 4

<img width="299" alt="image" src="https://github.com/mbbelizaire21/Data-Mining-in-R-Food-Mart-/assets/125572462/b67f3864-753f-4575-85d1-5d9c3fc70b7e">

K = 6

<img width="306" alt="image" src="https://github.com/mbbelizaire21/Data-Mining-in-R-Food-Mart-/assets/125572462/d4462038-06ad-4c94-bbdd-e794884879f9">

K = 8 

<img width="298" alt="image" src="https://github.com/mbbelizaire21/Data-Mining-in-R-Food-Mart-/assets/125572462/e57d0c4f-87c3-44db-86fa-7ad1a4a220cc">





# Conclusion
This project provides valuable insights into retail sales, customer behavior, and the effectiveness of media promotions. The analysis includes visualizations, association rules, and clustering patterns. Food Mart has used 13 different media types, each with varying costs. Analyzing the effectiveness of these media types in promoting their products can help them identify the most suitable ones for different customer groups. For instance, using Association Rule Mining, they found that Product Attachment is cost-effective for targeting frequent customers, building loyalty through discount coupons. Decision Tree models can help decide which media types to focus on based on cost ranges, but large datasets may affect accuracy. K-Means can group similar media types, enabling better budget allocation. Ultimately, Food Mart can choose the most appropriate method for analysis based on their objectives and specific cost ranges, gaining insights into customer behavior and optimizing media usage.

# How to Use the Code
Install R and RStudio.
Clone or download this repository to your local machine.
Ensure that the "media prediction and its cost.csv" file is placed in the correct directory/folder.
Open the R_Code.R file in RStudio.
Run the code step by step to perform data analysis and visualization.
