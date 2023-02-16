# PCA Analaysis of US Arrests Dataset

## Description:
This project uses PCA and two clustering methods to make predictions on the US Arrests Dataset.

## Table of Contents
- [Installation](#inst)
- [Usage Instructions - PCA](#pca)
- [Usage Instructions - KMeans](#kmeans)
- [Usage Instructions - Hierarchical](#hierarchical)
- [Credits](#creds)


<a name="inst"></a>
## 1. Installation

### Import Packages for dataframe, visualisations and models:
- import pandas as pd
- import numpy as np
- import seaborn as sns
- import matplotlib.pyplot as plt
- %matplotlib inline
- from sklearn.preprocessing import StandardScaler
- from sklearn.decomposition import PCA
- from sklearn.metrics import accuracy_score, silhouette_score
- from sklearn.cluster import AgglomerativeClustering
- from scipy.cluster.hierarchy import dendrogram, linkage

### Import CSV
The CSV can be found here: [UsArrests.csv](https://github.com/KateEGosling/finalCapstone/files/10760453/UsArrests.csv)

<a name="pca"></a>
## 2. PCA analysis:
- Create a scree plot to identify optimal number of components
- Look at the shape of curve to determine optimum number of components. For example in the image below, you can see  >80% of variance is explained by PCs: 0, 1 and 2 
<img width="344" alt="Scree plot" src="https://user-images.githubusercontent.com/123898068/219483888-213d4061-352f-4d51-8bc6-06c8490e24ba.PNG">

- Using optimal number of components, carry out PCA to remove redundancies
- Plot correlation heatmap post-PCA for visual confirmation that redundancies have been removed
<img width="390" alt="PCA plot" src="https://user-images.githubusercontent.com/123898068/219483737-b25de010-76eb-4c9d-af3c-62c38f8e7061.PNG">


<a name="kmeans"></a>
## 3. Cluster analysis 1 - KMeans:
- Create an elbow plot to identify optimum number of clusters for Kmeans model. Optimal number is where there is an 'elbow' in the line and the gradient begins to flatten - in this case, 4
<img width="413" alt="Elbow plot" src="https://user-images.githubusercontent.com/123898068/219483936-f12f0296-93b5-4e2a-ad12-3e49ee3ad233.PNG">
- Plost clusters of KMeans model using the optimum number of clusters
<img width="344" alt="Kmeans plot" src="https://user-images.githubusercontent.com/123898068/219483906-5069b950-e956-4ca2-8372-ffceda7fe3bc.PNG">

<a name="hierarchical"></a>
## 4. Cluster analysis 2 - Hierarchical:
- Use dendrogram plots to identify whether complete vs average, and euclidean or cityblock paramters should be used. Imagining a horizontal line through the graph at the point of the tallest line, then counting how many vertical lines cross shows how many clusters - in this case, 4
<img width="341" alt="Dendrograms" src="https://user-images.githubusercontent.com/123898068/219483943-a6896681-a96b-4eaf-aecd-f49e2380dbba.PNG">
- Plost clusters of Hierarchical model using the chosen parameters and number of clusters
<img width="333" alt="hierarchical scatter" src="https://user-images.githubusercontent.com/123898068/219483923-362ee0bf-6bf0-42dc-9b47-6b78602419c7.PNG">

<a name="creds"></a>
## 5. Credits
HyperionDev for support in teaching me the skills needed for this project.
