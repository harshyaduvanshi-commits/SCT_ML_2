# Customer Segmentation using K-Means Clustering

## Project Overview
This project groups mall customers into distinct segments based on their
purchase behavior, using the **K-Means Clustering** algorithm on the Kaggle
"Mall Customers" dataset. The goal is to identify which customers are the
best targets for marketing efforts.

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn

## Workflow
1. Load and explore the dataset (200 customers, 5 features)
2. Visually compare feature pairs to identify which combination shows
   natural clustering
3. Select Annual Income and Spending Score as clustering features
4. Apply feature scaling (StandardScaler)
5. Use the Elbow Method to choose the optimal number of clusters (K)
6. Train the K-Means model
7. Visualize the resulting customer segments
8. Evaluate cluster quality using the Silhouette Score
9. Interpret each cluster in plain business terms

## Dataset
- Source: Kaggle "Customer Segmentation Tutorial" (Mall_Customers.csv)
- 200 customer records
- Features: CustomerID, Gender, Age, Annual Income (k$), Spending Score (1-100)

## Features Used for Clustering
- Annual Income (k$)
- Spending Score (1-100)

Age and Gender were explored but not used in the final clustering, since
Age did not show clear separable groupings when visually compared against
the other features (see Feature Selection step).

## Evaluation
- Elbow Method (WCSS) to select K
- Silhouette Score to measure cluster separation and cohesion

## Results
K-Means with K=5 produced clearly separable customer segments based on
income and spending behavior (update with your actual Silhouette Score).
The clusters were interpreted into business-friendly segments, including
identifying a "High Income - High Spending" group as the primary target
customers for marketing campaigns.

## Limitations
- Clustering was performed using only 2 of the 4 available features
  (Annual Income and Spending Score); Age and Gender were not incorporated
  into the final model
- The number of clusters (K) was chosen using the Elbow Method, which can
  be somewhat subjective to interpret
- Cluster labels are not inherently ordered or ranked - they are arbitrary
  group identifiers assigned by the algorithm

## Future Improvements
- Incorporate Age and/or Gender into the clustering to see if more nuanced
  segments emerge
- Compare cluster quality across multiple values of K using Silhouette Score,
  not just the Elbow Method
- Automate cluster labeling (e.g. sort clusters by mean spending score)
  instead of manually matching labels after each run
- Try alternative clustering algorithms (e.g. Hierarchical Clustering, DBSCAN)
  for comparison

---
