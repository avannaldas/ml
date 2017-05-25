---
layout: post
title:  "Decoding Regularized Greedy Forest"
date: 2017-04-09
---

In my last post, we discussed about Decision Trees, Ensemble methods and Gradient Boosted Decision Trees. In this post, we will look at a few limitations of Gradient Boosted Decision Trees and how does Regularized Greedy Forest tackle with those with the improvements it proposes.

### Limitations of Gradient Boosted Decision Trees (GBDT)
* No explicit regularization. Though, there is some doubt/debate<sup>[1]</sup> that the learning rate and early stopping rounds together interact to act (implicitly) to regularize.
* Infinitesimally small shrinkage parameter <i>s</i> aka learning rate, is required to achieve good performance.
* Small learning rate, used implicitly for Regularization, may lead to huge model size which increases the computational cost, both for training and prediction.
* Each individual tree learner is treated as a black box, where it only returns the decision rules based on basis function. Hence, the tree learning and forest learning doesn't happen together.

## Regularized Greedy Forest

_explanation_

_formal definition_













<sup>[1] More about this on page 4 in the paper titled <I>Learning Nonlinear Functions Using Regularized Greedy Forest<I> by Rie Johnson and Tong Zhang</sup>
