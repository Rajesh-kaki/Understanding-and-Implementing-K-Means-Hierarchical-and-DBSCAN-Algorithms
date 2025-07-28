# Understanding-and-Implementing-K-Means-Hierarchical-and-DBSCAN-Algorithms


This project applies three popular clustering algorithms — K-Means, Hierarchical Clustering, and DBSCAN — on airline customer data to uncover patterns in frequent flyer behavior. It includes detailed preprocessing, visualization, and model comparison.

## 🧠 What is Clustering?
Clustering is an unsupervised machine learning technique used to group similar data points into clusters based on their features. It is widely used in customer segmentation, anomaly detection, and data exploration.

📁 Dataset Description
Dataset: EastWestAirlines.xlsx

Rows: Each row represents a customer

Columns: Include features like:

Balance: Total frequent flyer points

Qual_miles: Qualifying miles flown

Bonus_miles, Flight_miles_12mo, Days_since_enroll, etc.

Removed identifiers (ID#) and target (Award?) columns before clustering.

## ⚙️ Workflow Summary
1. Data Preprocessing
Dropped unnecessary columns like ID#, Award?

Scaled features using StandardScaler for uniformity across variables

📊 Clustering Algorithms Implemented
## 🔹 1. K-Means Clustering
Concept: Partitions data into k clusters by minimizing intra-cluster distance.

Steps Taken:

Scaled data using StandardScaler

Used Elbow Method to find optimal k

Applied KMeans() from sklearn with optimal number of clusters

Why K-Means? It is efficient for large datasets and assumes spherical clusters.

## 🔹 2. Hierarchical Clustering
Concept: Builds a hierarchy of clusters either in a bottom-up (agglomerative) or top-down (divisive) fashion.

Steps Taken:

Computed linkage matrix with ward method

Visualized dendrogram to determine number of clusters

Used AgglomerativeClustering for final grouping

Why Hierarchical? It doesn't require predefined number of clusters and is interpretable via dendrogram.

## 🔹 3. DBSCAN (Density-Based Spatial Clustering)
Concept: Forms clusters based on dense regions of points and separates outliers as noise.

Steps Taken:

Used DBSCAN() from sklearn

Tuned eps and min_samples for meaningful grouping

Why DBSCAN? Useful for identifying clusters of arbitrary shapes and handling noise.

🧪 Evaluation and Interpretation
Visualizations: Pairplots and 2D projections were used to interpret clusters

Labels: Cluster labels were appended to the original dataset for profiling

Comparison: Compared number of clusters and customer distribution across methods

🛠️ Libraries Used
pandas, numpy – data manipulation

matplotlib, seaborn – visualizations

scikit-learn – clustering algorithms and scaling

scipy.cluster.hierarchy – dendrogram and linkage

📂 Files
Clustering.ipynb — Main notebook with step-by-step clustering implementation

EastWestAirlines.xlsx — Dataset used for segmentation

## 📌 Key Takeaways
K-Means performed well after feature scaling, with clear cluster separation

Hierarchical clustering gave insights into the natural grouping of customers

DBSCAN detected outliers and allowed flexible cluster formation without predefining k
