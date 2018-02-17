---
layout: post
title:  "Introduction to Ensemble Learning Methods in ML"
date: 2017-06-03
---

Machine Learning is advancing at a rapid pace day by day. It never ceases to surprise with newer breakthroughs from time to time. Be it IBM Watson's jeopardy win or a recent win of DeepMind's Alpha Go over a human expert in the game of Go. It is certainly the next revolution in the history of mankind after industrial revolution. Andrew Ng, best known for his introductory Machine Learning course, has rightly said - AI is the new electricity! It comes with unimaginable opportunities, only to be discovered by time.

Many data science competition winning solutions nowadays are built using techniques known as Ensemble Learning. Dictionary meaning of Ensemble is a _group_. Likewise in ML, Ensemble refers to multiple (different) Machine Learning models working together as a group. In real life too, we know that a group is always intelligent than an individual. It's a quite natural to believe a piece of information that comes from multiple sources. We do look for multiple opinions at times in real life when one expert opinion isn't convincing enough for us to act upon. It's somewhat similar idea in Machine Learning. 

While any type of ML algorithms can be used with ensembling techniques, most often, some form of Decision Trees and/or random forests are used with ensembling techniques. In this post, we'll go through a quick introduction of Information Entropy, Decision Trees and popular ensemble techniques.

#### __Decision Tree and Information Entropy__ 
Entropy is a measure of impurity/noise in data. When we navigate through the data reducing noise to find a piece of information/truth, we say that we have reached a pure form of data, meaning zero entropy. 

Say for example we have data of all flight departures from a particular airport for last one year. Data like - airline carrier, departure gate, departure time, aircraft model and delayed. There could be many more, but let's consider these for now. Now, given this information for future flights, we would want to predict if the aircraft was _delayed_. The existing data in our case has some entropy. And when we segregate the data into two buckets based on whether the flight was delayed, we can say we have data with zero impurity in this particular case.

It might seem straight foward to identify items in these two buckets, just split based on whether the flight was _delayed_. But the point here is, for future flights that piece of information would be missing we cannot do this split easily due to the information impurity (entropy).

We use decision trees to uncover the circumstances in which the flight was delayed, though we don't have _delayed_ information, we do have information (other fields) which gives some idea of _delayed_. To give a quick idea of how decision trees do it, consider this, we notice that 8 in every 10 flights departed from a particular gate were delayed (may be because of the airport plan and gate's location). Now, if we make two buckets based on whether the flight departure was from that particular gate or not, we have a bucket where 80% of flights will possibly be delayed and while we don't know much about the other bucket. This additional information that we uncovered is known as information gain (reduction in entropy). And when for future flight departures from that particular gate, we know that there is an 80% chance that the flight would be delayed. Decision trees learn to ask the right questions in the right order to identify items in these buckets as fast as possible, i.e., maximizing information gain (entropy reduction) in least possible steps (questions/splits). With every split, decision tree knows the probabiliy of each outcome (delayed or not delayed) for both the branches of the split. Usually these set (or more correctly, sequence) of questions (conditions identified) generalize so as to predict fairly accurate for future flights.

#### __Ensemble Methods__
Some of the common Ensemble Learning techniques are...

__Bagging__: Trains on a subset of samples iteratively and results are combined. The results can be combined in many ways, for instance a majority vote for classification and average for regression. Learn more <A href="https://en.wikipedia.org/wiki/Bootstrap_aggregating" target="_blank">here</A>.

__Boosting__: Trains iteratively, each time improving prediction on previous misclassified observations. Learn more <A href="https://en.wikipedia.org/wiki/Boosting_(machine_learning)" target="_blank">here</A>.

__Stacking__: Multiple algorithms are trained and the outputs (predictions) become features for the final model, sometimes referred to as meta learner. Learn more <A href="https://en.wikipedia.org/wiki/Ensemble_learning#Stacking" target="_blank">here</A>.


#### Further Learning
* <A href="https://www.khanacademy.org/computing/computer-science/informationtheory" target="_blank">Information Theory</A>
* <A href="https://en.wikipedia.org/wiki/Entropy_(information_theory)" target="_blank">Information Entropy</A>
* <A href="https://en.wikipedia.org/wiki/Information_gain_in_decision_trees" target="_blank">Information Gain</A>
* <A href="https://en.wikipedia.org/wiki/Ensemble_learning" target="_blank">Ensemble Learning</A>
* <A href="https://en.wikipedia.org/wiki/Gradient_boosting" target="_blank">Gradient Boosting</A>
* <A href="https://xgboost.readthedocs.io/en/latest/" target="_blank">XGBoost</A>
* <A href="https://github.com/Microsoft/LightGBM" target="_blank">LightGBM</A>
* <A href="http://docs.h2o.ai/h2o/latest-stable/h2o-docs/data-science/gbm.html" target="_blank">H2O</A>
* <A href="https://www.import.io/post/how-to-win-a-kaggle-competition/" target="_blank">Blog post about winning Kaggle competitions</A>

#### Mentioned in post
* <A href="https://en.wikipedia.org/wiki/Andrew_Ng" target="_blank">Andrew Ng</A>
* <A href="https://www.coursera.org/learn/machine-learning" target="_blank">Andrew Ng's Machine Learning Course</A>
* <A href="https://twitter.com/andrewyng/status/735874952008589312?lang=en" target="_blank">AI is the new electricity!</A> tweet by Andrew Ng
* <A href="https://en.wikipedia.org/wiki/AlphaGo" target="_blank">AlphaGo</A>
* <A href="https://en.wikipedia.org/wiki/Watson_(computer)#Jeopardy.21" target="_blank">IBM Watson winning jeopardy</A>

