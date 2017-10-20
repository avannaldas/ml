---
layout: post
title:  "DBSCAN Clustering"
date: 2017-10-20
---

### Density Based Spatial Clustering of Applications with Noise (DBSCAN)

DBSCAN is a different type of clustering algorithm with some unique advantages. As the name indicates, this method focuses more on the proximity and density of observations to form clusters. This is very different from KMeans, where an observation becomes a part of cluster represented by nearest centroid. DBSCAN clustering can identify outliers, observations which won't belong to any cluster. Since DBSCAN clustering identifies the number of clusters as well, it is very useful with unsupervised learning of the data when we don't know how many clusters could be there in the data.

K-Means clustering may cluster loosely related observations together. Every observation becomes a part of some cluster eventually, even if the observations are scattered far away in the vector space. Since clusters depend on the mean value of cluster elements, each data point plays a role in forming the clusters. Slight change in data points _might_ affect the clustering outcome. This problem is greatly reduced in DBSCAN due to the way clusters are formed.

In DBSCAN, clustering happens based on two important parameters viz., 
  * __neighbourhood (n)__ - cutoff distance of a point from (core point -- discussed below) for it to be considered a part of a cluster. Commonly referred to as _epsilon_ (abbreviated as _eps_).
  * __minimum points (m)__ - minimum number of points required to form a cluster. Commonly referred to as _minPts_.

There are three types of points after the DBSCAN clustering is complete viz.,
  * __Core__ - This is a point which has at least _m_ points within distance _n_ from itself.
  * __Border__ - This is a point which has at least one Core point at a distance _n_.
  * __Noise__ - This is a point which is neither a Core nor a Border. And it has less than _m_ points within distance _n_ from itself.
  
DBSCAN clustering can be summarized in following steps...
  1. For each point _P_ in dataset, identify points _pts_ within distance _n_.
     * if _pts_ >= _m_, label _P_ as a _Core_ point
     * if _pts_ < _m_ and a core point is at distance _n_, label _P_ a _Border_ point
     * if _pts_ < _m_, label _P_ a _Noise_ point
   2. For the sake of explainability, lets refer to __a _Core_ point and all the points within distance _n___ as a Core-Set. All the overlapping Core-Sets are grouped together into one cluster. Like multiple individual graphs being connected to form a set of connected graphs.

<p style="text-align:center">
<img style="max-width:100%;" src="https://github.com/avannaldas/avannaldas.github.io/raw/master/uploads/dbscan.png" />
</p>

Since clustering entirely depends on the parameters _n_ and _m_ (above), choosing these values correctly is very important. While good domain knowledge of the subject helps choosing good values for these parameters, there are also some approaches where these parameters can be fairly approximated without deep expertise in the domain.

See DBSCAN demo in <A href="http://scikit-learn.org/stable/auto_examples/cluster/plot_dbscan.html" target="_blank">sklearn examples</A> and try it with <A href="http://scikit-learn.org/stable/modules/generated/sklearn.cluster.DBSCAN.html" target="_blank">sklearn.cluster.DBSCAN</A> in sklearn.

