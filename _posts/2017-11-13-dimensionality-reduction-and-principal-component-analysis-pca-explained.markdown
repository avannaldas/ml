---
layout: post
title:  "Dimensionality Reduction and Principal Component Analysis (PCA) Explained"
date: 2017-11-13
---

Data is seldom clean and ready for machine learning or predictive modelling. Data preprocessing is time consuming and non-trivial effort in any predictive modelling task. A recent <a href="https://www.kaggle.com/surveys/2017" target="_blank">kaggle survey</A> says that dirty data is a biggest barrier!

Once the data is cleaned and pre-processed, the next challenge is finding the important features of the data, engineering new features and ignoring less important or _irrelevant_ features for the predictive modelling task at hand. Not every piece of data is equally important and may not be relevant in context of the problem being solved. Some attributes may be noise or duplication in some form, and sometime a particular transformation of an attribute (or engineered feature) could be much more relevant than an original attribute.

Popular ways to find these important features are...
  1. Hand crafted feature engineering - deriving features based on existing features, domain expertise and sometimes <A href="#a" title="We need to be careful with data augmentation, check for data leak">data augmentation</A>.
  2. Feature Selection - selecting a subset of important features, ignoring features that don't contribute towards predictions.
  3. Dimensionality Reduction (we'll discuss PCA in this post) - a type of linear transformations of attributes.
 
Of the above three, sometimes any one strategy might suffice or a combination of all three could be used. If all three strategies are used, I believe the above sequence is an appropriate approach, please share in comments what do you think.

PCA has several advantages. It helps find the most effective transformation of existing attributes through a linear transformation technique. It helps with dimensionality reduction, which makes things faster by reducing the size of dataset to be stored and processed. PCA, with dimensionality reduction, also makes visualization easy to some extent as it's hard to visualize and understand data anything beyond 3 dimensions. Intuitively we can say -- _It is a change in viewpoint (linear transformation) of a scene (vector space), which gives much clear shot of the objects (data) in the scene!_ 

Let's consider an analogy for some intuition, a business which sells flooring products for homes needs some insights. Let's consider two pieces (as it makes it easy to draw and visualize) of information about the real estate data viz., plot length and plot width of the house.

![House Plot Length and Width](https://raw.githubusercontent.com/avannaldas/avannaldas.github.io/master/uploads/pca-1.png "Original Attributes")

Before doing PCA, the data is normalized by substracting mean and usually scaled, data looks something like this after normalizing

![House Plot Length and Width Scaled](https://raw.githubusercontent.com/avannaldas/avannaldas.github.io/master/uploads/pca-2.png "Normalized data")

PCA identifies two principal components, represented by red and orange lines below.

![Principal Components](https://raw.githubusercontent.com/avannaldas/avannaldas.github.io/master/uploads/pca-3.png "Two Principal Components")

In this case, PCA identified an attribute what seems to be analogous to plot area, without we engineering the feature ourselves. It seems little obvious in this case due to the nature of chosen example, but PCA does find dimensions (attributes) that aren't always obvious to us. 

Now, let's understand how does PCA work.

PCA finds a linear transformation which __maximizes variance__. This is done by minimizing the projection error along the data. This is known as principal component, and the subsequent components are mutually orthogonal. Each principal component is an eigenvector. In the below diagram, green lines are projections from blue data points onto red line, the first principal component. I've reduced the number of data points from previous diagram to make it easy to show, as well as draw :), projections.

![Projection Error](https://raw.githubusercontent.com/avannaldas/avannaldas.github.io/master/uploads/pca-4.png "Projection error shown with green projections for first principal component")

PCA finds the most important to least important dimensions. So it's possible that the last/later dimensions have eigen values close to zero. Hence, when we choose _k_ of the _n_ dimensions, we get the _k_ most important dimensions. 

Computing PCA has three main steps...
  1. Compute covariance matrix of all the attributes
  2. Perform SVD on the covariance matrix computed in step 1
  3. Step two returns three matrices viz., _U_, _S_ and _V_. Matrix _U_ is a _n_ x _n_ matrix, where _n_ is the number of total  dimensions/principal components. We choose first _k_ columns of the matrix, which represent _k_ dimensions we need.

#### Dimensionality Reduction vs Feature Selection
With PCA we pick _k_ (most important) dimensions of _n_ dimensions. _k_ is a parameter determined based on problem and experience. These _k_ attributes are optimal to represent the insights, derive correlations and predictions.

Feature Selection on other hand is picking a subset of all features (and engineered features) of higher importances. Importance can be calculated using different techniques. Some of the popular techniques are available in <A href="http://scikit-learn.org/stable/modules/feature_selection.html" target="_blank">sklearn</A> and sometimes, the learning algorithm provides the importances of different features.

These two techniques are very different from each other. While dimensionality reduction finds the best features, they aren't actual features (attributes) we could relate to, they are all linear transformations of existing features. Hence it's difficult to understand what drives those predictions and outcomes. On the contrary, with feature selection selection, we have much better understanding of the attributes/features and their significance w.r.t. outcome.

Thanks for reading, please share your thoughts in comments.
