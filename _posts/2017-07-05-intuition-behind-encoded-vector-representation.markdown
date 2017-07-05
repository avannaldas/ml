---
layout: post
title:  "Intuition Behind Encoded Vector Representation"
date: 2017-07-05
---
In this post I will share the intuition behind the encoded vectors, like One Hot Encoding used for categorical variables and word embeddings used to represent words in Natural Language Processing. We always represent non-numeric data in terms of vectors for very obvious reason. Non-numeric values cannot be used in the computations required to learn/predict the patterns with Machine Learning. 

These computations are almost always about operations on vectors in multi-dimensional space (hyperspace). All the attributes of the data need to be represented using numeric values in the form of a vector. Sometimes when the attribute is not numeric in nature, doesn't have a magnitude/scale or anything such sort of, we encode the values in terms of vectors. 

Categorical values would be encoded as one hot vector, in other words it is a unit-vector pointing along only one axis/dimension in the hyperspace. On the other hand, a single encoded word embedding is a vector (may nor may not be a unit-vector), but it usually points into hyperspace based on the dimensions it represents. For example, if dimensions are animal, pet, fur, etc. dog and cat could be represented using similar or same vectors based on the word embedding strategy. If it is representing a single word in vocabulary, it can be a unit-vector pointing along a single axis the word is represented by.

Two things happen when non-numeric values are encoded. First, the encoded attribute adds new dimensions to the hyperspace equal to the number of all possible distict values the attribute it is encoding. Secondly, these vectors help in clustering together similar observations (records) as they affect the representation of an observation in hyperspace.

Every encoding adds multiple dimensions to the hyperspace the problem is being solved in. Every encoding adds to the level of complexity. To make it explicit, imagine a number-line. Add a dimension, it's an X-Y plane. Add one more dimension, it's an X-Y-Z space. Add one more dimension, and it's a hyperspace. Beyond this it's hard to intuitively imagine the representation of an hyperspace. And it adds to the complexity of solving a problem. It goes without saying that we should exercise caution while adding encoded representations. 

This post is a result of sudden realization of the intuition behind encoded vector representation. These thoughts are all about how I understand this. I could be incorrect. Please let me know what do you think in comments. Your comments will help anyone who lands here, including me. It's all about learning from each other, isn't it?
