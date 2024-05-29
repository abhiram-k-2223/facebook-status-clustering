# Facebook Status Clustering

## Project Overview

Welcome to the Facebook Status Clustering project! This repository contains code to perform clustering on Facebook status updates using machine learning techniques. The project focuses on preprocessing the data, applying K-means clustering, and evaluating the results to understand the natural groupings within the data.

## Dataset

The dataset used in this project contains Facebook status updates with various features, including the type of status, the time it was published, and other attributes.

## Steps Involved

### 1. Data Loading and Preprocessing

- **Loading the Data:** The dataset is loaded using Pandas.
- **Initial Adjustments:** The `status_id` column is dropped, and the `status_published` column is converted to datetime format.
- **Handling Duplicates:** Duplicate entries are identified and removed to ensure data quality.

### 2. Feature Transformation

- **One-Hot Encoding:** The `status_type` categorical feature is one-hot encoded.
- **Datetime Features Extraction:** The `status_published` datetime column is split into separate year, month, day, hour, and minute columns.
- **Dropping Original Datetime Column:** The original `status_published` column is removed after extracting relevant features.

### 3. Clustering with K-Means

- **Within-Cluster Sum of Squares (WCSS):** Calculated for different numbers of clusters to determine the optimal number using the elbow method.
- **K-Means Clustering:** Applied with the optimal number of clusters.
- **Cluster Assignment:** Each data point is assigned to a cluster.

### 4. Visualization and Evaluation

- **Pair Plot:** Seaborn pair plot is used to visualize the clusters and their relationships.
- **Cluster Centroids:** The centroids of the clusters are printed for analysis.
- **Silhouette Score:** Calculated for different numbers of clusters to evaluate the clustering performance.

## Results

The project demonstrates the clustering of Facebook status updates into distinct groups based on their features. The optimal number of clusters is determined using the elbow method and silhouette score.

## How to Use

1. **Clone the Repository:** `git clone https://github.com/abhiram-k-2223/facebook-status-clustering.git`
2. **Navigate to the Directory:** `cd facebook-status-clustering`
4. **Run the Notebook:** Execute the Jupyter notebook to perform clustering and visualize the results.
