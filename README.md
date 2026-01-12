# Spotify Audio Features Clustering Project

## Overview

This project applies **unsupervised machine learning techniques** to cluster Spotify songs based on their audio features. The goal is to discover meaningful patterns and groupings in music data without using predefined labels.

The project explores multiple clustering algorithms and dimensionality reduction techniques to compare performance, interpretability, and visualization quality.

---

## Objectives

* Perform clustering using different unsupervised learning models
* Compare clustering performance and behavior across models
* Reduce dimensionality for visualization and efficiency
* Interpret and analyze resulting clusters

---

## Dataset

* **Source:** Spotify audio features dataset
* **Data Type:** Numerical audio features (e.g., tempo, energy, loudness, danceability)
* **Preprocessing Steps:**

  * Selection of numerical features
  * Handling missing values
  * Feature scaling using StandardScaler

---

## Models Implemented

### 1. K-Means Clustering

* Centroid-based clustering algorithm
* Partitions data into *k* clusters based on Euclidean distance
* Evaluated using:

  * Elbow Method
  * Silhouette Score

**Finding:** Optimal number of clusters was **k = 3**

---

### 2. Hierarchical Clustering

* Agglomerative (bottom-up) clustering approach
* Uses Ward linkage method
* Produces a dendrogram to visualize cluster hierarchy

**Use Case:**

* Understanding relationships between clusters
* Exploratory analysis

---

### 3. DBSCAN (Density-Based Clustering)

* Groups points based on density
* Identifies noise and outliers
* Does not require specifying the number of clusters in advance

**Advantages:**

* Detects irregular cluster shapes
* Robust to noise

**Limitations:**

* Sensitive to parameter selection (eps, min_samples)

---

### 4. Gaussian Mixture Model (GMM)

* Probabilistic clustering approach
* Assumes data is generated from multiple Gaussian distributions
* Allows soft cluster assignments

**Advantages:**

* Handles overlapping clusters
* Provides probability-based membership

---

## Dimensionality Reduction

### Principal Component Analysis (PCA)

* Reduces high-dimensional data to 2 components
* Preserves maximum variance
* Used for visualization and computational efficiency

### t-SNE (t-Distributed Stochastic Neighbor Embedding)

* Non-linear dimensionality reduction
* Captures local structure in data
* Used to visualize clusters in 2D space

---

## Model Evaluation

Since clustering is unsupervised, evaluation relied on intrinsic methods:

* **Elbow Method:** Determines optimal number of clusters for K-Means
* **Silhouette Score:** Measures cluster cohesion and separation
* **Cluster Distribution Analysis:** Examines balance and size of clusters
* **Visualization:** PCA and t-SNE plots for interpretability

---

## Key Results

* **K-Means (k = 3)** achieved the best balance between simplicity and performance
* GMM provided flexible, probabilistic clustering
* DBSCAN effectively detected outliers
* PCA and t-SNE significantly improved cluster visualization

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib

---

## Conclusion

This project demonstrates how unsupervised learning can uncover hidden patterns in music data. By comparing multiple clustering techniques, we gain deeper insights into song similarity and structure, enabling applications such as music recommendation and playlist generation.

---

## Future Improvements

* Hyperparameter tuning for DBSCAN and GMM
* Incorporating additional audio or metadata features
* Evaluating clustering stability
* Deploying results in a recommendation system

