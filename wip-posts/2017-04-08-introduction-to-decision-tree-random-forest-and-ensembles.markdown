---
layout: post
title:  "Introduction to Decision Trees, Random Forest and Ensembles"
date: 2017-04-08
---

Machine Learning is advancing at a rapid pace today. It is certainly the next revolution in the history of mankind after industrial revolution. <A href="https://en.wikipedia.org/wiki/Andrew_Ng" target="_blank">Andrew Ng</A>, best known as the founder of <A href="https://www.coursera.org/" target="_blank">Coursera.org</A> someone who has introduced <A href="https://www.coursera.org/learn/machine-learning" target="_blank">Machine Learning</A> to millions, has rightly said - <A href="https://twitter.com/andrewyng/status/735874952008589312?lang=en" target="_blank">AI is the new electricity!</A>. It comes with unimaginable opportunities, only to be discovered by time.

A significant number of data science competition <A href="https://www.import.io/post/how-to-win-a-kaggle-competition/" target="_blank">winning solutions</A> today are built using one of the forms of Decision Trees/Random Forest. XGBoost is one of the hottest Ensemble methods today. I've recently learnt about <A href="https://arxiv.org/pdf/1109.0887" target="_blank">Regularized Greedy Forest</A>, which is relatively new form of Ensemble method. Read about Regularized Greedy Forest in detail in my next post.

In this post, I'll briefly introduce about some foundational stuff- Decision Trees and Ensemble Methods (Decision Forest).

## Information Entropy
With decision trees, we are trying to find some information/knowledge with the data we have and would want to apply it to our present/future conditions/scenarios. We ask questions based on existing data and arrive at a conclusion. The number of questions that we need to ask to arrive at a conclusion/truth, is directly proportional to the Entropy. Entropy is a measure of upredictability of the state of a piece of information. 

Entropy is a measure of impurity/noise in data. When we navigate through the data reducing noise to find a piece of information/truth, we say that we have reached a pure form of data.

## Decision Trees
At the most fundamental level, Decision Trees are a series of very efficient if-then-else decisions, similar to a programming construct. If you are new to Machine Learning, let me give an analogy. Think for a moment, how would you code when there are 10 variables you need to consider and code based on their values for different cases. Most likely, you'd code so as to keep the nesting/complexity to the minimum. Decision Trees too ensure that the tree depth remains minimum. The actual decisions within the tree, aren't just Yes/No decisions. Every decision has associated weights/probabilities to it. Probabilities which indicate probability of one of the two child/subsequent cases becoming true. This is also known as Information Gain in decision trees. Information Gain can be intuitively understood as the increasing level of understanding about of piece of information (based on decision branches, formed on the basis of historical data) and confidence (probability) as we move through different branches within the tree trying to uncover some truth or a fair prediction.

---Start-Formal Definition

- information gain can be represented by...

---End-Formal Definition


## Ensemble Methods (Decision Forest)
Ensembles are another way of using Decision Trees. Ensemble, literally means a group. And hence Ensemble of Decision Trees is known as Decision Forest. So why do we want to group together multiple trees? It's a quite natural to believe a piece of information that comes from multiple sources. We do look for multiple opinions when one expert opinion isn't enough when we want to be doubly sure. Ensembles do the same thing. It takes into consideration what multiple trees predict on a particular decision. And the majority decision by all those trees combined is considered final.

There are multiple types of Ensembles, based on how trees/forest is formed and the inner workings. Some of the popular ones are...
* <A href="https://en.wikipedia.org/wiki/AdaBoost" target="_blank">AdaBoost</A>
* <A href="https://en.wikipedia.org/wiki/Bootstrap_aggregating" target="_blank">Bagging</A>
* <A href="https://en.wikipedia.org/wiki/Random_forest" target="_blank">Random Forest</A>
* <A href="https://en.wikipedia.org/wiki/Boosting_(machine_learning)" target="_blank">Boosting</A>
* <A href="https://en.wikipedia.org/wiki/Gradient_boosting" target="_blank">Gradient Boosting</A>

Of all these, Gradient Boosting technique is the latest and usually the most efficient. In this post, we'll breifly discuss what is Gradient Boosting.

## Gradient Boosted Decision Trees (GBDT)
Gradient boosted decision trees at the most basic level learn from minimizing error of a nonlinear prediction function.

Gradient Boosted Decision Trees accept 3 parameters viz., (1) number of terminals J (leaves), (2) number of trees K (iterations) and (3) Shrinkage rate s (Learning Rate)

At each step, after the tree is built, the coefficients of the J leaves are updated before updating the resulting hypothesis based on the shrinkage rate.

_give better explanation for GBDT_

---Start-Formal Definition

---End-Formal Definition





