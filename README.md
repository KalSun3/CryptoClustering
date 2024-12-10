# CryptoClustering
Cryptocurrency Clustering Analysis
This project performs a cluster analysis on cryptocurrency data based on their price change percentages over different time intervals (24 hours and 7 days). The goal is to group similar cryptocurrencies using K-Means clustering and analyze how reducing the feature space with Principal Component Analysis (PCA) impacts the clustering results.

Project Overview
The project involves the following steps:

1. Data Preprocessing
The cryptocurrency dataset is first scaled using StandardScaler to ensure that all features are on the same scale before applying clustering algorithms.
2. Elbow Method for Optimal Number of Clusters (k)
The elbow method is used to determine the optimal number of clusters (k). The model is run with different values of k (from 1 to 11), and the inertia (sum of squared distances from points to their cluster center) is calculated. The "elbow" point in the plot indicates the best value for k.
3. Clustering with K-Means (Original Data)
The K-Means clustering algorithm is applied to the scaled dataset, grouping cryptocurrencies based on their price changes.
A scatter plot is created to visualize the resulting clusters, with price_change_percentage_24h on the x-axis and price_change_percentage_7d on the y-axis. Points are color-coded by cluster, and cryptocurrency names are shown on hover.
4. Principal Component Analysis (PCA)
PCA is performed on the scaled data to reduce the dimensionality of the features to three principal components.
The explained variance of each principal component is computed to understand how much information is retained after the dimensionality reduction.
5. Clustering with K-Means (PCA-Reduced Data)
The K-Means clustering algorithm is then applied to the PCA-reduced data, and the resulting clusters are visualized in a scatter plot using the first two principal components (PC1 and PC2).
6. Comparison of Results
A comparison is made between the inertia values from the elbow method for both the original scaled data and the PCA-reduced data.
A visual comparison of the clustering results is also provided, showing how the clusters differ when using the original data versus the PCA-reduced data.
7. Analysis
The impact of using fewer features (via PCA) on the clustering results is analyzed, and conclusions are drawn about the effectiveness of dimensionality reduction in the K-Means clustering process.
Files and Functionality
crypto_market_data.csv: The raw cryptocurrency data containing features such as price change percentages.
Crypto_Clustering.ipynb: The Jupyter notebook containing the code for the entire analysis process, including data preprocessing, clustering, PCA, and visualizations.
Requirements
Python 3.x
Pandas
Scikit-learn
Matplotlib
Hvplot
How to Run
Clone this repository to your local machine.
Install the required libraries by running:
bash
Copy code
pip install -r requirements.txt
Open the Crypto_Clustering.ipynb notebook and run the cells to perform the analysis.
Questions and Insights
What's the best value for k?
What is the total explained variance of the three principal components?
What is the impact of using fewer features to cluster the data using K-Means?
