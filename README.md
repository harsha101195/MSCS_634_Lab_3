# Lab 3: Clustering Analysis Using K-Means and K-Medoids

## Purpose

The purpose of this lab was to explore unsupervised machine learning
techniques by implementing the K-Means and K-Medoids clustering
algorithms on the Wine dataset from scikit-learn. The dataset was first
standardized using z-score normalization before applying both clustering
algorithms. Their performance was evaluated using the Silhouette Score
and the Adjusted Rand Index (ARI), followed by a visual comparison of
the resulting clusters using a two-dimensional PCA projection.

## Key Results

  Algorithm     Silhouette Score   Adjusted Rand Index
  ----------- ------------------ ---------------------
  K-Means                 0.2849                0.8975
  K-Medoids               0.2676                0.7411

## Key Insights

-   Standardizing the features was essential because the Wine dataset
    contains measurements with different scales. Without normalization,
    features with larger numeric ranges would dominate the distance
    calculations.
-   K-Means produced the strongest clustering performance in this
    experiment. It achieved both a higher Silhouette Score and a
    substantially higher Adjusted Rand Index, indicating more compact
    clusters and better agreement with the true wine classes.
-   K-Medoids generated slightly less compact clusters and a lower ARI.
    While it is generally more robust to outliers because cluster
    centers are actual observations, this advantage was not significant
    for the Wine dataset.
-   PCA was used only for visualization. The clustering itself was
    performed on the full 13-dimensional standardized dataset, while PCA
    projected the data into two dimensions to make the clusters easier
    to interpret visually.

## Conclusion

The experimental results demonstrate that K-Means is the better choice
for the Wine dataset because the data contains relatively compact,
well-separated clusters with few influential outliers. K-Medoids remains
a useful alternative for datasets containing noisy observations or
significant outliers, although it generally incurs higher computational
cost.
