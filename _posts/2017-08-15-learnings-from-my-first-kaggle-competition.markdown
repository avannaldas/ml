---
layout: post
title:  "Learnings from my first kaggle competition"
date: 2016-08-08
---

My first Kaggle competition <A href="https://www.kaggle.com/c/instacart-market-basket-analysis/" target="_blank">Instacart Market Basket Analysis</A> has concluded. Though my ranking wasn't impressive, I've learned a lot in this competition, from everyone. I'm happy that I know quite a few things after this competition.

Here are few things I learned in this competition. I've missed some of these this time, hoping to do better on next time.

* Begin with understanding data and then spend maximum time on feature engineering initially. Start with a notebook and pen. Hoping to leave no stone unturned. Feature engineering is something that should never need more time at later point of time. Though feature engineering ideas can come at any point of time, in my opinion separating this crucial step as first milestone helps in concentrating on building final solution. Validate the merges/joins are happening the way they are intended to happen.
* It's important to use the correct evaluation metric during the model training.
* Use the cross validation strategy (when) available natively with the library rather than doing it separately.
* Don't use small early stopping for XGBoost, LightGBM, etc.
* Always keep one more held out set apart from the cross validation set used with model training, cross validation scoring. Score on different metrics with held out set.
* Keep training iterations (n_estimators, epochs) small, a little bigger learning rate when just evaluating results/improvement locally, saves a lot of time. Can be fine tuned when required.
* Create a custom data loader for large datasets which can load appropriately sampled train and multiple evaluation datasets specified in percentage, can be very useful when playing around with different models and approaches with such large datasets. This was my biggest roadblock as I was working towards the end of competition with such huge dataset. Sampling smaller dataset would have saved a lot of time. When working on such huge datasets its easy to exhaust even 32GB RAM.
* Work on two different approaches simultaneously if it's gonna take a large amount of time to train.
* When writing a submission file, always write a text file with the details like model, parameters and details that help you reproduce it (I once hit the logloss of 0.20+ but wasn't able to reproduce it again).
* Feature importance and feature selection are different for algorithm (like what LightGBM thinks is important may not be true with XGBoost) hence Feature selection (elimination) should be based on the model/algorithm.
* To gain the most out of the competition, it helps to focus on learning one thing. In this competition, the solution could have been a time-series based, based on Deep Neural Network, based on ensembling techniques, based on feature engineering, etc. Focusing on learning one thing may not win the competition but eventually leads to invaluable learning of something new. In this competition, I focused on stacking multiple models, feature selection and hyper-parameter tuning. These things didn't give me a good rank in the competition but I learned those things.
