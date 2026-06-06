Hierarchical Clustering
Definition

Hierarchical Clustering is an unsupervised machine learning algorithm that groups similar data points into clusters and builds a hierarchy (tree structure) of clusters.

It creates a Dendrogram, which helps visualize how clusters are formed.

Types of Hierarchical Clustering
1. Agglomerative Clustering (Bottom-Up)
Start with each data point as a separate cluster.
Merge the two closest clusters repeatedly.
Continue until only one cluster remains.
2. Divisive Clustering (Top-Down)
Start with all data points in one cluster.
Split clusters repeatedly.
Continue until each point becomes a separate cluster.
Agglomerative Clustering Algorithm
Step 1

Treat every data point as an individual cluster.

Step 2

Calculate the distance matrix between all clusters.

Step 3

Find the two closest clusters.

Step 4

Merge those clusters.

Step 5

Update the distance matrix.

Step 6

Repeat Steps 3–5 until one cluster remains.

Step 7

Cut the dendrogram at a chosen height to obtain the required number of clusters.

Linkage Methods
Single Linkage

Distance between the nearest points of two clusters.

d(C
1
	​

,C
2
	​

)=mind(x,y)
Advantages
Detects non-spherical clusters.
Disadvantages
Chaining effect.
Sensitive to noise.
Complete Linkage

Distance between the farthest points of two clusters.

d(C
1
	​

,C
2
	​

)=maxd(x,y)
Advantages
Produces compact clusters.
Disadvantages
Breaks large clusters early.
Average Linkage

Average distance between all pairs of points.

d(C
1
	​

,C
2
	​

)=
∣C
1
	​

∣∣C
2
	​

∣
1
	​

∑d(x,y)
Advantages
Balanced approach.
Less sensitive to outliers.
Ward's Method

Minimizes the increase in within-cluster variance.

Δ=
∣C
1
	​

∣+∣C
2
	​

∣
∣C
1
	​

∣∣C
2
	​

∣
	​

∣∣μ
1
	​

−μ
2
	​

∣∣
2
Advantages
Produces compact clusters.
Most commonly used method.
Dendrogram

A dendrogram is a tree-like diagram used to visualize cluster formation.

Important Points
Leaves represent data points.
Branches represent cluster merges.
Height indicates distance between merged clusters.
A horizontal cut determines the number of clusters.
Rule

Number of branches crossing the cut line = Number of clusters.

Distance Metrics
Euclidean Distance

d(x,y)=
∑
i
	​

(x
i
	​

−y
i
	​

)
2
	​


Most commonly used.
Suitable for continuous numerical data.
Manhattan Distance

d(x,y)=∑
i
	​

∣x
i
	​

−y
i
	​

∣

More robust to outliers.
Cosine Distance
d(x,y)=1−
∣∣x∣∣∣∣y∣∣
x⋅y
	​

Commonly used for text clustering.
Mahalanobis Distance
d(x,y)=
(x−y)
T
S
−1
(x−y)
	​

Considers feature correlations.
Complexity
Time Complexity
Naive Implementation: O(n³)
Optimized Version: O(n² log n)
Space Complexity
O(n²)
Hierarchical Clustering vs K-Means
Feature	Hierarchical	K-Means
Need K beforehand	No	Yes
Deterministic	Yes	No
Output	Dendrogram	Cluster Labels
Time Complexity	O(n² log n) to O(n³)	O(nKt)
Scalability	Small datasets	Large datasets
Cluster Shape	Flexible	Spherical
Advantages
No need to specify K initially.
Produces dendrogram.
Deterministic results.
Works well for small datasets.
Disadvantages
High computational cost.
Sensitive to outliers.
Not suitable for very large datasets.
Merges cannot be undone.
Applications
Gene Expression Analysis
Customer Segmentation
Document Clustering
Image Segmentation
Market Analysis
Social Science Research
Phylogenetic Tree Construction
