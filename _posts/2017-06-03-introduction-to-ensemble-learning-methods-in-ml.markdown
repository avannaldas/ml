---
layout: post
title:  "Introduction to Ensemble Learning Methods in ML"
date: 2017-06-03
---

Machine Learning is advancing at a rapid pace day by day. It never ceases to surprise with newer breakthroughs from time to time. Be it IBM Watson's jeopardy win or a recent win of DeepMind's Alpha Go over a human expert in the game of Go. It is certainly the next revolution in the history of mankind after industrial revolution. Andrew Ng, best known for his introductory Machine Learning course, has rightly said - AI is the new electricity! It comes with unimaginable opportunities, only to be discovered by time.

A significant number of data science competition winning solutions today are built using various advanced forms of Decision Trees (or Ensembles of Random Forest techniques to be more correct). Ensembles in ML context can be understood in one liner as - combination of different decision trees/random forest predictors.

In this post, I'll briefly introduce about some basics about Decision Trees, Random Forest and Ensemble Methods.

#### Information Entropy
With decision trees, we are trying to find some information/knowledge with the data we have and would want to apply it to our present/future conditions/scenarios. We ask questions based on existing data to reduce information entropy (noise) and reveal some information in pure form (meaning zero entropy). The number of questions that we need to ask to arrive at a conclusion/truth, is directly proportional to the Entropy.

Entropy is a measure of impurity/noise in data. When we navigate through the data reducing noise to find a piece of information/truth, we say that we have reached a pure form of data, meaning zero entropy.

#### Decision Trees
At the most fundamental level, decision trees are a series of very efficient if-then-else decisions (and much more infact!), similar to a programming construct. If you are new to Machine Learning, think of an analogy. How would you code when there are 10 variables you need to consider and code based on their values for different cases? Most likely, you'd code so as to keep the nesting/complexity to the minimum. Decision Trees too ensure that the tree depth remains minimum. The actual decisions within the tree, aren't just Yes/No decisions. Every decision has associated weights/probabilities to it which has the information about both left and right subtrees and their entropy level. Probability at a particular tree node indicates a chance of particular outcome at that level and below in a tree. At every decision in the tree, the reduction in entropy is known as Information Gain. Information Gain can be intuitively understood as the increasing level of understanding about of piece of information. In ML the decision tree is built based on historical data and quest for a particular piece of information about new data is met using the decision tree, to uncover some truth or a fair prediction of an event or value of something. This piece of information (event or value) is known as target variable. A decision tree can help find value/probability/fair guess of a target variable it was built for, based on other data points involved.

#### Ensemble Methods (Decision Forest)
Ensembles are another way of using Decision Trees. Ensemble, literally means a group. And hence Ensemble of Decision Trees is known as Decision Forest. So why do we want to group together multiple trees? It's a quite natural to believe a piece of information that comes from multiple sources. We do look for multiple opinions at times in our daily life when one expert opinion isn't convincing enough for us to act upon. Ensembles do the same thing. It takes into consideration what multiple trees predict on a particular decision. And the majority decision by all those trees combined is considered final.

There are many ways decision trees ensembles work, based on how individual decision tree results are considered, weighted, evaluated and combined.

Some of the popular ensemble methods are <A href="https://en.wikipedia.org/wiki/AdaBoost" target="_blank">AdaBoost</A>, <A href="https://en.wikipedia.org/wiki/Bootstrap_aggregating" target="_blank">Bagging</A>, <A href="https://en.wikipedia.org/wiki/Random_forest" target="_blank">Random Forest</A>, <A href="https://en.wikipedia.org/wiki/Boosting_(machine_learning)" target="_blank">Boosting</A> and <A href="https://en.wikipedia.org/wiki/Gradient_boosting" target="_blank">Gradient Boosting</A>. Of all these, Gradient Boosting technique (Gradient Boosted Decision Trees) is the latest and usually the most efficient. Some of the popular implementations of Gradient Boosted Decision Trees are available in libraries XGBoost, LightGBM and H2O to name a few.

#### Further Learning
* <A href="https://www.khanacademy.org/computing/computer-science/informationtheory" target="_blank">Information Theory</A>
* <A href="https://en.wikipedia.org/wiki/Entropy_(information_theory)" target="_blank">Information Entropy</A>
* <A href="https://en.wikipedia.org/wiki/Information_gain_in_decision_trees" target="_blank">Information Gain</A>
* <A href="https://en.wikipedia.org/wiki/Ensemble_learning" target="_blank">Ensemble Learning</A>
* <A href="https://en.wikipedia.org/wiki/Gradient_boosting" target="_blank">Gradient Boosting</A>

#### Mentioned in post
* <A href="https://en.wikipedia.org/wiki/Andrew_Ng" target="_blank">Andrew Ng</A>
* <A href="https://www.coursera.org/learn/machine-learning" target="_blank">Andrew Ng's Machine Learning Course</A>
* <A href="https://xgboost.readthedocs.io/en/latest/" target="_blank">XGBoost</A>
* <A href="https://github.com/Microsoft/LightGBM" target="_blank">LightGBM</A>
* <A href="http://docs.h2o.ai/h2o/latest-stable/h2o-docs/data-science/gbm.html" target="_blank">H2O</A>
* <A href="https://twitter.com/andrewyng/status/735874952008589312?lang=en" target="_blank">AI is the new electricity!</A> tweet by Andrew Ng
* <A href="https://www.import.io/post/how-to-win-a-kaggle-competition/" target="_blank">Blog post about winning Kaggle competitions</A>
* <A href="https://en.wikipedia.org/wiki/AlphaGo" target="_blank">AlphaGo</A>
* <A href="https://en.wikipedia.org/wiki/Watson_(computer)#Jeopardy.21" target="_blank">IBM Watson winning jeopardy</A>
