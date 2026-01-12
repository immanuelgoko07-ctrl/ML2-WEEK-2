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




## 1. Data Preparation

* Selected **numerical features only**
* Handled missing values
* Applied **StandardScaler** to normalize feature scales (essential for distance-based models)

---

## 2. K-Means Clustering

### a) Elbow Method

* Tested **k = 2 to 5**
* Inertia decreases sharply up to **k = 3**, then flattens
  ✅ **Optimal k ≈ 3**

### b) Silhouette Score

* Highest silhouette score also occurs at **k = 3**
* Confirms good separation and compact clusters

**Conclusion:**
👉 **K-Means with 3 clusters** provides the best balance between cohesion and separation.

---

## 3. Hierarchical Clustering (Conceptual Analysis)

* Agglomerative (Ward linkage) approach
* Useful for understanding **hierarchical relationships between songs**
* Helps identify how smaller clusters merge into larger ones

**Use case:**
✔ Exploratory analysis
✔ Understanding similarity structure

---

## 4. DBSCAN

* Density-based clustering
* Identifies:

  * Core clusters
  * **Noise / outliers** (songs with unusual audio patterns)
* Advantage:

  * No need to specify number of clusters
  * Handles irregular cluster shapes

**Limitation:**
Sensitive to `eps` and `min_samples`

---

## 5. Gaussian Mixture Model (GMM)

* Probabilistic clustering
* Each song assigned a **probability of belonging** to each cluster
* Suitable when clusters overlap

**Advantage:**
✔ More flexible than K-Means
✔ Captures uncertainty in cluster membership

---

## 6. Dimensionality Reduction & Visualization

### a) PCA (Principal Component Analysis)

* Reduced data to **2 dimensions**
* Preserved maximum variance
* Useful for:

  * Visual inspection
  * Improving clustering efficiency

### b) t-SNE

* Non-linear dimensionality reduction
* Reveals **local structure and natural groupings**
* Ideal for **visual interpretation** of clusters

---

## 7. Cluster Distribution & Interpretability

* Compared cluster sizes across:

  * K-Means
  * DBSCAN
  * GMM
* Ensured clusters are:

  * Balanced
  * Meaningful
  * Not dominated by noise

---

## 8. Key Takeaways

| Model        | Strength              | Best Use                |
| ------------ | --------------------- | ----------------------- |
| K-Means      | Simple, fast          | Well-separated clusters |
| Hierarchical | Interpretability      | Exploratory analysis    |
| DBSCAN       | Noise detection       | Outlier-heavy data      |
| GMM          | Probabilistic         | Overlapping clusters    |
| PCA          | Variance preservation | Visualization           |
| t-SNE        | Local structure       | Cluster visualization   |

---

## Final Recommendation

✔ Use **K-Means (k = 3)** as the primary clustering model
✔ Use **GMM** for probabilistic insights
✔ Use **PCA + t-SNE** for visualization and interpretation


<img width="580" height="455" alt="8ce92d26-148c-4c5b-a3a7-1854b9076c3b" src="https://github.com/user-attachments/assets/5a104c1e-5a9b-47d2-9abf-91fa385b5d28" />
<img width="584" height="455" alt="2d530679-6e81-427c-b902-d4059dd33301" src="https://github.com/user-attachments/assets/2d1aff80-0f2c-4139-bcb3-8f0edf334d6e" />

