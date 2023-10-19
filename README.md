# CryptoClustering
Module 19 Challenge

In this (data analysis project)[https://github.com/aliciahlavac/CryptoClustering/blob/main/Crypto_Clustering.ipynb], we begin by preparing and normalizing cryptocurrency data from a CSV file using the StandardScaler module from scikit-learn. We then create a DataFrame with the scaled data, setting the "coin_id" index from the original DataFrame as the index for the new DataFrame.

Next, we employ the elbow method to determine the optimal number of clusters (k) for our K-Means clustering. We create a list of k values ranging from 1 to 11, compute the inertia (within-cluster sum of squares) for each value of k, and plot an elbow curve to visually identify the best k value.

With the best k value in hand, we proceed to perform K-Means clustering using the original scaled data. We initialize the K-Means model and fit it with the data, predicting clusters to group cryptocurrencies. We then visualize the results by creating a scatter plot using hvPlot, where we set the x-axis as "PC1" and the y-axis as "PC2" and color the graph points with the cluster labels obtained from K-Means. We add the "coin_id" column in the hover_cols parameter to identify each cryptocurrency.

Furthermore, we explore Principal Component Analysis (PCA) on the original scaled data to reduce features to three principal components. We retrieve the explained variance to assess how much information can be attributed to each principal component.

To fine-tune our clustering, we utilize the elbow method once more, but this time on the PCA data, to identify the optimal k value. After determining the best k value, we initialize the K-Means model and fit it using the PCA data. We predict the clusters to group cryptocurrencies and visualize the results with a scatter plot created using hvPlot. In this case, the x-axis is set as "price_change_percentage_24h," the y-axis as "price_change_percentage_7d," and the graph points are colored according to the K-Means cluster labels. We include the "coin_id" column in the hover_cols parameter to identify each cryptocurrency represented in the plot. This project involves comprehensive data preprocessing, optimal k value determination, K-Means clustering, and visualization using both the original scaled data and PCA data, providing valuable insights into cryptocurrency patterns and groupings.
