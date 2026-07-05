# E-Commerce Customer Churn Prediction & Segmentation

A Data Mining project that analyzes an e-commerce customer dataset (5,600+ records) 
to predict churn and segment customers into actionable groups using clustering, 
optimization, and fuzzy logic techniques.

## Problem Statement
Customer churn is costly in e-commerce. This project identifies at-risk customer 
segments and recommends personalized cashback bonuses to maximize Customer 
Lifetime Value (CLV).

## Pipeline Overview
1. **Exploratory Data Analysis (EDA)** - distribution analysis, correlation 
   heatmaps, churn patterns by tenure, cashback, and product category
2. **Data Preprocessing** - missing value imputation, outlier capping (IQR), 
   one-hot encoding, feature scaling (StandardScaler)
3. **Dimensionality Reduction** - PCA to reduce the feature space for 
   visualization and clustering
4. **K-Medoids Clustering** - optimal k selected using Elbow Method and 
   Silhouette Score; produced 3 distinct customer segments
5. **Hierarchical Clustering** - applied on GA-optimized features with 
   Single, Complete, and Average linkage; compared against K-Medoids results
6. **Genetic Algorithm (GA)** - used for feature selection to maximize 
   clustering quality (silhouette score) across 30+ encoded features
7. **Fuzzy Logic Inference System** - takes K-Medoids and Hierarchical 
   cluster scores as inputs and recommends a bonus cashback percentage 
   per customer segment
8. **End-to-End Pipeline** - accepts a single customer record and outputs 
   cluster label + recommended cashback bonus

## Customer Segments Identified
- **New Dissatisfied Customers** - short tenure, high complaint rate
- **Engaged Mid-Value Customers** - moderate loyalty, growth potential
- **High-Value Loyal Customers** - long tenure, high cashback, low churn risk

## Tech Stack
Python, Pandas, NumPy, Scikit-learn, sklearn-extra (KMedoids), 
SciPy (Hierarchical Clustering), Matplotlib, Seaborn

## Note
Data Mining academic team project.
