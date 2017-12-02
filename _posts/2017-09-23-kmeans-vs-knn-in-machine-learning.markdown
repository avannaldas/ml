---
layout: post
title:  "K-Means vs KNN"
date: 2017-09-23
---

# K-Means vs KNN

K-Means (K-Means Clustering) and KNN (K-Nearest Neighbour) are often confused with each other in Machine Learning. In this post, I'll explain some attributes and some differences between both of these popular Machine Learning techniques.
<br/>


|                    K-Means                       |              KNN               |
|--------------------------------------------------|--------------------------------|
| It is an __Unsupervised__ learning technique | It is a __Supervised__ learning technique |
| It is used for __Clustering__ | It is used mostly for __Classification__, and sometimes even for __Regression__ |
| 'K' in K-Means is the number of clusters the algorithm is trying to identify/learn from the data. The clusters are often unknown since this is used with Unsupervised learning. | 'K' in KNN is the number of nearest neighbours used to classify or (predict in case of continuous variable/regression) a test sample |
| It is typically used for scenarios like understanding the population demomgraphics, market segmentation, social media trends, anomaly detection, etc. where the clusters are unknown to begin with. | It is used for classification and regression of known data where usually the target attribute/variable is known before hand. |
| In training phase of K-Means, K observations are arbitrarily selected (known as centroids). Each point in the vector space is assigned to a cluster represented by nearest (euclidean distance) centroid. Once the clusters are formed, for each cluster the centroid is updated to the mean of all cluster members. And the cluster formation restarts with new centroids. This repeats until the centroids themselves become mean of clusters, i.e., when updating centroids to mean doesn't change them. The prediction of a test observation is done based on nearest centroid. | K-NN doesn't have a training phase as such. But the prediction of a test observation is done based on the K-Nearest (often euclidean distance) Neighbours (observations) based on weighted averages/votes. |

<br />
<i>You can find a bare minimum KMeans algorithm implementation from scratch <A href="https://github.com/avannaldas/ML-from-scratch/blob/master/avlearn/cluster.py" target="_blank">here</A>.</i>
<br /><br />
<i>Learn more about <A href="https://en.wikipedia.org/wiki/K-means_clustering" target="_blank">K-Means Clustering</A> and <A href="https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm" target="_blank">K-Nearest Neighbors</A></i>
