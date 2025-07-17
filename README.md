# Bank Transaction Anomaly Detection Using DBSCAN

## Project Overview

This project applies the **DBSCAN** (Density-Based Spatial Clustering of Applications with Noise) clustering algorithm to a real-world bank transaction dataset to detect anomalous or potentially fraudulent transactions. Using features such as withdrawal amount, deposit amount, and account balance, the DBSCAN model groups similar transactions into clusters and flags unusual transactions as outliers (noise).

## What is DBSCAN?

DBSCAN is an **unsupervised machine learning algorithm** used for clustering data based on density. Unlike other clustering methods, DBSCAN does not require specifying the number of clusters upfront. It groups points that are closely packed together while marking points in low-density regions as noise or outliers.

Key advantages of DBSCAN:

- Can find clusters of arbitrary shape.
- Identifies noise points that do not belong to any cluster.
- Requires two main parameters:
  - **`eps`**: the maximum distance between two samples to be considered neighbors.
  - **`min_samples`**: the minimum number of points required to form a dense cluster.

## Dataset

The dataset used consists of bank transactions with columns including:

- Withdrawal Amount
- Deposit Amount
- Account Balance
- Transaction Date and other metadata

Missing values are handled carefully to ensure data quality before clustering.

## Project Workflow

1. **Data Loading and Cleaning**  
   The Excel dataset is loaded and cleaned by removing irrelevant columns and filling or dropping missing values appropriately.

2. **Feature Selection and Scaling**  
   Numeric features relevant to transaction behavior (`WITHDRAWAL AMT`, `DEPOSIT AMT`, `BALANCE AMT`) are selected and standardized to prepare for clustering.

3. **DBSCAN Clustering**  
   The DBSCAN model is applied with tuned parameters (`eps` and `min_samples`) to identify clusters of similar transactions and detect outliers.

4. **Result Interpretation and Visualization**  
   Results are visualized with scatter plots showing transaction groups and outliers. Noise points (outliers) represent suspicious or unusual transactions that merit further investigation.

## Interpreting Results After Training

- **Clusters**: Groups of transactions sharing similar patterns, such as small frequent withdrawals or large deposits.
- **Noise (Outliers)**: Transactions not fitting any cluster, potentially indicating fraud or errors.
- **Visualizations**: Scatter plots help in understanding the distribution and density of transaction types.


