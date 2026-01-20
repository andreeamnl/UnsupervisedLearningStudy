# UnsupervisedLearningStudy

# Mall Customers Clustering Study

## Overview

This repository contains a small comparative study on the Mall Customers Dataset.  
The goal is to explore how different unsupervised learning algorithms group customers based on their demographic and behavioral features.

Four clustering methods are implemented and analyzed:

- K-Means
- Agglomerative Clustering (Hierarchical)
- DBSCAN
- Expectation-Maximization (Gaussian Mixture Models)

Cluster quality is evaluated using the Silhouette Score and supported by visual inspection.

---

## Dataset

The dataset includes customer information collected from a shopping mall, with the following features:

- CustomerID
- Gender
- Age
- Annual Income
- Spending Score

These features are used to identify natural customer segments.

The dataset can be found at https://www.kaggle.com/datasets/shwetabh123/mall-customers

---

## Methods

### K-Means

K-Means is a centroid-based clustering algorithm that partitions the data into a predefined number of clusters by minimizing intra-cluster variance.

### Agglomerative Clustering

Agglomerative Clustering is a hierarchical method that starts with each data point as its own cluster and merges clusters step by step based on similarity.  
The results are visualized using a dendrogram to show the hierarchical structure of the clusters.

### DBSCAN

DBSCAN is a density-based clustering algorithm that groups points in dense regions and labels low-density points as noise.  
This method does not require specifying the number of clusters in advance.

### Expectation-Maximization (GMM)

The Expectation-Maximization algorithm, implemented through Gaussian Mixture Models, assumes that the data is generated from a mixture of Gaussian distributions.  
It performs soft clustering by assigning probabilities of cluster membership to each data point.

---

## Evaluation

### Silhouette Score

The Silhouette Score is used to measure how well each data point fits within its assigned cluster compared to other clusters.

The score ranges from -1 to +1:

- Values close to +1 indicate well-separated and compact clusters.
- Values around 0 suggest overlapping clusters.
- Negative values indicate potential misclassification.

The final score is computed as the mean silhouette score across all data points.

---

## Results

The clustering algorithms were compared using silhouette scores and visualizations.

In general:

- K-Means produced compact clusters with reasonable separation.
- Agglomerative Clustering revealed a clearer hierarchical structure and achieved a higher silhouette score than K-Means.
- DBSCAN successfully detected noise points but struggled with clusters of varying density.
- EM (GMM) handled overlapping clusters and provided probabilistic cluster assignments.

Exact silhouette scores and plots can be found in the corresponding notebooks.

---

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Jupyter Notebook

---

## Conclusion

This study shows how different clustering algorithms behave on the same dataset and highlights the importance of using evaluation metrics such as the Silhouette Score when selecting a clustering approach.

No single algorithm performed best in all aspects; the choice of method depends on the data distribution and the intended interpretation of the clusters.

---

## Author

Andreea Manole
