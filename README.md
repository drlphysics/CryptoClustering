# CryptoClustering
## Overview
This project focuses on clustering cryptocurrencies using K-Means and optimizing clusters with Principal Component Analysis (PCA). The objective is to identify patterns and group similar cryptocurrencies based on various performance metrics. The project follows a structured approach to load, preprocess, and analyze the data using clustering algorithms and PCA.

## Repository Structure
CryptoClustering/
│
├── Resources/
│   ├── crypto_market_data.csv
│
├── Crypto_Clustering_starter_code.ipynb
│
├── README.md

## Instructions
### Step 1: Load and Prepare the Data
Objective: Load the cryptocurrency market data and prepare it for analysis.

Rename the Crypto_Clustering_starter_code.ipynb file to Crypto_Clustering.ipynb.
Load the crypto_market_data.csv file into a DataFrame and set the index to the “coin_id” column.
Get the summary statistics to understand the data.
Output: Summary statistics of the loaded data.

### Step 2: Normalize the Data
Objective: Normalize the data using the StandardScaler from scikit-learn.

Use the StandardScaler module to normalize the data.
Create a new DataFrame with the scaled data and set the "coin_id" index from the original DataFrame.
Output: Scaled DataFrame with the first five rows displayed.

### Step 3: Find the Best Value for k Using the Original Scaled Data
Objective: Determine the optimal number of clusters (k) using the elbow method.

Create a list with k values from 1 to 11.
Create an empty list to store inertia values.
Use a for loop to compute the inertia for each k value.
Create a dictionary with the data to plot the elbow curve.
Plot the elbow curve to identify the optimal k value.
Output: Elbow curve plot and determination of the best k value.

### Step 4: Cluster Cryptocurrencies with K-Means Using the Original Scaled Data
Objective: Cluster the cryptocurrencies using the K-Means algorithm based on the best k value.

Initialize the K-Means model with the best k value.
Fit the model using the original scaled DataFrame.
Predict the clusters and add a new column with the predicted clusters to the original data.
Create a scatterplot with "price_change_percentage_24h" on the x-axis and "price_change_percentage_7d" on the y-axis.
Output: Scatterplot showing clustered cryptocurrencies based on the original scaled data.

### Step 5: Optimize Clusters with Principal Component Analysis
Objective: Use PCA to reduce the data to three principal components and optimize clustering.

Perform PCA on the original scaled DataFrame.
Retrieve the explained variance for each principal component.
Create a new DataFrame with the PCA data and set the "coin_id" index.
Answer the question: What is the total explained variance of the three principal components?
Output: PCA DataFrame and explained variance analysis.

### Step 6: Find the Best Value for k Using the PCA Data
Objective: Determine the optimal number of clusters (k) for the PCA data using the elbow method.

Create a list with k values from 1 to 11.
Create an empty list to store inertia values.
Use a for loop to compute the inertia for each k value.
Create a dictionary with the data to plot the elbow curve.
Plot the elbow curve to identify the optimal k value.
Answer the questions: What is the best value for k when using the PCA data? Does it differ from the best k value found using the original data?
Output: Elbow curve plot for PCA data and determination of the best k value.

### Step 7: Cluster Cryptocurrencies with K-Means Using the PCA Data
Objective: Cluster the cryptocurrencies using the K-Means algorithm based on the PCA data and the best k value.

Initialize the K-Means model with the best k value.
Fit the model using the PCA DataFrame.
Predict the clusters and add a new column with the predicted clusters to the PCA data.
Create a scatterplot with "PC1" on the x-axis and "PC2" on the y-axis.
Answer the question: What is the impact of using fewer features to cluster the data using K-Means?
Output: Scatterplot showing clustered cryptocurrencies based on the PCA data.

### Step 8: Determine the Weights of Each Feature on Each Principal Component
Objective: Analyze the influence of each feature on the principal components.

Create a DataFrame showing the weights of each feature for each principal component.
Answer the question: Which features have the strongest positive or negative influence on each component?
Output: DataFrame showing feature weights for each principal component.