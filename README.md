# CryptoClustering
#### Data Preparation
- Loaded the cryptocurrency market data from `crypto_market_data.csv` into a DataFrame.
- Examined the summary statistics and plotted the data to visualize its structure.
- Normalized the data using StandardScaler from scikit-learn.
- Created a DataFrame with the scaled data and set the "coin_id" as the index.

#### Finding the Best Value for k Using the Original Scaled DataFrame
- Implemented the elbow method to determine the optimal value for k.
- Plotted a line chart to visualize the inertia values for different values of k.
- Concluded that the best value for k is {best_k}.

#### Clustering Cryptocurrencies with K-Means Using the Original Scaled Data
- Initialized a K-means model with {best_k} clusters.
- Fit the K-means model using the original scaled DataFrame.
- Predicted the clusters to group the cryptocurrencies and added a new column with the predicted clusters.
- Created a scatter plot using hvPlot to visualize the clusters.

#### Optimizing Clusters with Principal Component Analysis (PCA)
- Performed PCA to reduce the features to three principal components.
- Determined the total explained variance of the three principal components.
- Created a new DataFrame with the PCA data and set the "coin_id" index.

#### Finding the Best Value for k Using the PCA Data
- Applied the elbow method on the PCA data to find the best value for k.
- Plotted a line chart to visualize the inertia values for different values of k.
- Concluded that the best value for k when using the PCA data is {best_k_pca}, which differs from the best value obtained using the original data.

#### Clustering Cryptocurrencies with K-Means Using the PCA Data
- Initialized a K-means model with {best_k_pca} clusters.
- Fit the K-means model using the PCA data.
- Predicted the clusters to group the cryptocurrencies and added a new column with the predicted clusters.
- Created a scatter plot using hvPlot to visualize the clusters based on PCA-transformed data.

#### Visualizing and Comparing the Results
- Created composite plots using hvPlot to contrast the elbow curves obtained from the original data and PCA data.
- Created another composite plot to compare the cryptocurrency clusters resulting from using the original data and PCA data.
- Analyzed the impact of using fewer features to cluster the data using K-means.

### Conclusion
Overall, the challenge involved preprocessing cryptocurrency market data, determining the optimal number of clusters using the elbow method, clustering cryptocurrencies with K-means, optimizing clusters using PCA, and visualizing and comparing the results to understand the impact of dimensionality reduction on clustering performance.
