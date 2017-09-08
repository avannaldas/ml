---
layout: post
title:  "Data preprocessing in Machine Learning"
date: 2017-09-08
---
Data preprocessing is an important step of solving every machine learning problem. Most of the datasets used with Machine Learning problems need to be processed / cleaned / transformed so that a Machine Learning algorithm can be trained on it. Most commonly used preprocessing techniques are very few like - missing value imputation, encoding categorical variables, Scaling, etc. These techniques are easy to understand. But when we actually deal with the data, things often get clunky. Every dataset is different and poses unique challenges.

In this post, I'm not explaining preprocessing techniques, but sharing a few tips based on my experiences.

* Too many nulls - When most (over 60% to 70%) of the values in a column are null, it's better to drop the column. This percentage/threshold can be decided based on problem and experience.

* Same values/skew - Sometimes, a majority of values in a column might be same values with very few different values. We need to check if the occurrence of such values is due to a skew in dataset or is it natural for that dataset. If it's skewed, dataset should be resampled (sub-sample or over-sample, as appropriate). If it's not a skew and the values occur naturally in that way, it's better to drop the column.

* Data types - Check the datatypes of the columns, particularly date columns and type cast appropriately.

* Missing value imputation - Usually median is used with numeric columns and mode with non-numeric columns.

* When column doesn't have missing values - It's possible that a column doesn't have any null values in the train dataset, but it's very possible that it might have null values in test dataset. Hence, it's important to review the columns/data and perform missing value imputation of all columns that can possibly have missing values, even if the train dataset doesn't have any missing values.

* Categorical Attributes - 
    * When the number unique values in a categorical column are too high, check the value counts of each of those values. Replace rarely occurring values together into a single value like 'Other' before encoding.
    * When number of unique values is huge and even the values are equally distributed, try to find some related values and see if the multiple categorical values can be clubbed into single (grouping), thereby reducing the count of categorical values.

* Related Attributes - If there multiple attributes with same information with different granularity, like city and state, it's better to keep columns like state and delete city column. Additionally, keeping both columns and assessing feature importance might help in eliminating one column.

![alt text][LEOHE]

<br /><br /><br />
Machine Learning Practitioners/Data Scientists - Please share your thoughts, anything you wanna add or do differently/better.
<br /><br /><br />

[LEOHE]: https://github.com/avannaldas/avannaldas.github.io/raw/master/uploads/Label-Encoder-vs-One-Hot-Encoder.png "LabelEncoder vs OneHotEncoder"
