# Star Types Classification: Unsupervised Machine Learning

## What is this project?
An analytical project focused on unsupervised machine learning to cluster and discover stellar profiles based on physical and thermodynamic properties (Temperature, Luminosity, Radius, Absolute Magnitude, Color, and Spectral Class). The study evaluates the performance of partitioning, hierarchical, and density-based algorithms to reproduce real astronomical classifications without prior knowledge of the labels.

## Key Features
* **Physical Criteria Preprocessing:** Ordinal encoding of spectral categorical variables, respecting the magnitude relationship of thermal energy and temperature.
* **Dimensionality Reduction (PCA):** Feature space transformation using Principal Component Analysis after applying standard scaling, retaining 85.22% of the original variance in an optimal 2D subspace for distance calculation.
* **Multiple Algorithm Evaluation:** Comprehensive comparison among varied algorithms: K-Means (optimized via the elbow method and Silhouette metric), Agglomerative Hierarchical Clustering (evaluation of complete, ward, and average linkage methods), and DBSCAN.
* **Custom Density Validation (DBCV):** Integration of a specialized mathematical script (Density-Based Clustering Validation) using `scipy.spatial` and mutual reachability distance graphs to tune DBSCAN's `eps` and `min_samples` hyperparameters, overcoming the geometric limitations of the Silhouette coefficient.
* **Astronomical Inference:** Analytical contrast of the generated algorithmic clusters (e.g., K-Means with k=6) with real stellar diagrams, successfully isolating coherent groups corresponding to Red Dwarfs, White Dwarfs, Supergiants, and Main Sequence stars.

## Tech Stack
* **Language:** Python 3
* **Machine Learning:** Scikit-Learn (KMeans, AgglomerativeClustering, DBSCAN, PCA, StandardScaler, OrdinalEncoder).
* **Advanced Calculus:** SciPy (csgraph, minimum_spanning_tree, dijkstra, linkage, dendrogram).
* **Analysis & Visualization:** Pandas, NumPy, Matplotlib.

## Installation and Usage
1. Clone the repository to your local environment.
2. Install the main project dependencies by running:
```bash
pip install pandas numpy scikit-learn scipy matplotlib
