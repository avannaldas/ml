---
layout: post
title:  "Significance of Interpretable Predictive Models"
date: 2017-07-21
---
Humans are have curious minds. We often tend to ask why something is the way it is. It's an innate quality that helps us understand things around, learn and grow.

In Machine Learning, when a predictive model (or a machine learning model) predicts something, we usually only get a confidence level associated with prediction in terms of probability. And beyond this, most of the predictive models aren't very explaining in nature. Every predictive algorithm answers _What?_ but most of them miss on answering _How?_ and _Why?_

Let us consider a problem of predicting a returning customer in a context of a business which sells personal computers, peripherals and accessories. The machine learning model is built on the past data comprising of details about customer transactions, demographics, etc. The model is built to predict if a customer will return to buy certain products. To come to this conclusion, the model first finds patterns (training phase) within the sample data (training dataset). When the model is used to predict for an unseen customer, the model finds which learned patterns does the unseen customer match with. Lets consider one unseen customer C's case...

* [Input] C has purchased an ulra-notebook that is typically bought by frequent travelling professionals {consider, we have all details like, order date, configuration, etc.}
* [Prediction] Customer C will be a returning customer, and he will buy product P.

From the above case, even if we know the complete details of customer C (which aren't included here for simplicity), like pc configuration, order details, date, cost, etc. we won't be able to make it out why would customer C return and buy product P.

If the business knows what does it take (patterns learned by model) for a customer to return and buy product P, it could be of an incredible value. Business can take decisions which will turn more customers into returning customers. Without that, all that the business can do is just maintain inventory for predicted demand or carry out targeted marketing. If we see the magnitude of impact here, predictions help encash on the returning customers, and on the other hand learned insights help business to retain more customers.

In this case, the underlying patterns and what model learnt can be visualized in the form of a decision tree explaining a series of events/criteria that led to this outcome, or at a much highler level, giving out reasoning in natural language. 

Predictive models today are interpretable to a varied extent, based on the nature of underlying model. Some of the models aren't interpretable at all, like deep neural networks. In next post, I'll write a quick intro about interpretability of few popular algorithms.
