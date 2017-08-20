---
layout: post
title: Getting Started with Machine Learning in one hour!
permalink: /getting-started-with-machine-learning-in-one-hour/
---
I was planning agenda for my one hour talk. Conveying the learning paths, setting up the environment and explaining the important machine learning concepts finally made it to agenda after a lot of contemplation and thought. I initially thought about various ways this talk could have been done including - hands on python with linear regression, explaining linear regression in detail, or just sharing my learning journey that I went through past 18 months almost. But I wanted to start something that leaves the audience with lots of new information and questions to work on. Create curiosity and interest in them. And I guess I was able to do that to a decent level. Basically, to get them started with Machine Learning. That's how this guide ended up being called _Getting Started with Machine Learning in one hour_.

The notes for the talk were great for an introductory learning path, but were structured only for myself to help with the talk. Hence I wrote a machine learning getting started guide out of it and here it is. I'm very happy the way this ended up taking shape and I'm excited to share this!

There are two main approaches to learn Machine Learning. Theoretical Machine Learning approach and Applied Machine Learning approach. I've written about it in my earlier [blog post](http://abhijitannaldas.com/applied-vs-theoretical-machine-learning.html).

### Theoretical Machine Learning
Below are the subjects that you can start with (ordered as I think they are appropriate). For theoretical approach of learning Machine Learning, below subjects should be studied with great rigor and in depths.

  1. Linear Algebra - [MIT](https://ocw.mit.edu/courses/mathematics/18-06-linear-algebra-spring-2010/), [IISc. Bangalore](http://nptel.ac.in/courses/111108066)
  2. Calculus - [Basics, Coursera](https://www.coursera.org/learn/calculus1), [Advanced, Coursera](https://www.coursera.org/learn/advanced-calculus)
  3. Probability and Statistics - [MIT](https://ocw.mit.edu/courses/mathematics/18-05-introduction-to-probability-and-statistics-spring-2014/)
  4. Statistical Learning Theory - [MIT](https://ocw.mit.edu/courses/brain-and-cognitive-sciences/9-520-statistical-learning-theory-and-applications-spring-2003/), [Stanford](https://lagunita.stanford.edu/courses/HumanitiesSciences/StatLearning/Winter2016/about)
  5. Machine Learning - [Coursera](https://www.coursera.org/learn/machine-learning), [Caltech](https://work.caltech.edu/telecourse)
  6. Programming language to implement machine learning research ideas.

The way forward could be reading research papers, implementing research work/new algorithms, developing expertise and picking a specialization further on to the research path.

### Applied Machine Learning
1. Good understanding of the basics of above subjects (1 to 4).
2. Machine Learning (imp concepts explained below): [Coursera](https://www.coursera.org/learn/machine-learning), [Caltech](https://work.caltech.edu/telecourse)
3. [Python](https://www.datacamp.com/courses/intro-to-python-for-data-science) or R Programming Language, as per your preference.
4. Learn to use popular machine learning, data manipulation and visualization libraries in the chosen programming language. I personally use Python programming language, hence I'll elaborate on that below.
5. Must know Python Libraries: [numpy](https://www.datacamp.com/community/tutorials/python-numpy-tutorial), [pandas](https://www.datacamp.com/community/tutorials/pandas-tutorial-dataframe-python), [scikit-learn](https://www.datacamp.com/community/tutorials/pandas-tutorial-dataframe-python), [matplotlib](https://www.datacamp.com/community/tutorials/matplotlib-tutorial-python)
6. Other popular python libraries: [LightGBM](https://github.com/Microsoft/LightGBM), [XGBoost](https://github.com/dmlc/xgboost), [CatBoost](https://catboost.yandex/)

### Quick Start Option
_If you want to get a taste of what is Machine Learning about and what it could be like. You can start this way for experimenting, getting quick hands on. Not an ideal way if you want to get serious about Data Science in long run._
1. Know Machine Learning Concepts Overview (below)
2. Learn Python or R
3. Understand and learn to use popular libraries in your language of choice

### Python Environment setup
1. Python
   * Python.org [Download](https://www.python.org/downloads/), [Learn](https://www.datacamp.com/courses/intro-to-python-for-data-science) OR
   * Anaconda [Download](https://www.continuum.io/downloads), [Learn](https://docs.continuum.io/anaconda/)
2. Code Editor / IDE
   * Visual Studio Code (Search and install python extension, pick the most downloaded one)
   * Notepad++
   * [Jupyter](http://jupyter.readthedocs.io/en/latest/install.html) (Installs with Anaconda)
3. Installing python packages
   * [Managing packages with pip, python's native tool](https://docs.python.org/3/installing/index.html): `pip install <package-name>`
   * [Managing packages with anaconda](https://conda.io/docs/using/pkgs.html): `conda install <package-name>`
4. Managing Python (native) virtual environments (if multiple environments are needed)
   * Create virtual environment: `python -m venv c:\path\to\env\folder`
   * Command help: `python -m venv -h`
   * Switch environments: `activate.bat` script located in the virtual environment folder
   * Python (native) virtual environments [documentation](https://docs.python.org/3/library/venv.html)
5. Managing Anaconda virtual environments (if multiple environments are needed)
   * Default conda environment - `root`
   * List available environments - `conda env list`
   * Create new environment - `conda create --name environment_name`
   * Switch to environment - `activate environment_name` or `source activate environment_name`
   * Anaconda virtual environments [documentation](https://conda.io/docs/using/envs.html)

### Machine Learning Concepts Overview
* __Machine Learning__: Is an approach to find patterns from a large set of data through a function _f(x)_ which effectively generalizes to unseen _x_ to find learned patterns in unseen data and make the inferences the Machine Learning Model was trained for.
* __Dataset__: Data being used to apply machine learning and find patterns from. For supervised type of machine learning applications, the dataset contains both _x_ (input/attributes/independent variables) and _y_ (target/labels/dependent variables) data. For unsupervised data it's just _x_, input and the output of the data is some sort of learned patterns (like clusters, groups, etc.)
* __Train set__: A subset of _Dataset_ fed to (train) machine learning algorithm to learn patterns
* __Evaluation / Validation / Cross Validation Set__: Subset of _Dataset_ not in _Train set_ used to evaluate how the machine learning algorithm is doing.
* __Test set__: _Dataset_ to predict learned insights for. For supervised problems, target/label _y_ like in _train set_ is to be predicted and hence it isn't a part of _train set_. For unsupervised, _train_ and _test_ sets can be identical.
* __Types__:
  * __Supervised__: In supervised problems, the historical data includes the labels (target attribute, outcomes) that need to be predicted for future/unseen data. For example, for housing price prediction we have data about house (area, # of bedrooms, location, etc.) and price. Here the after training a machine learning model with given data (X - data) and price (Y - labels), in future, price (Y) will be predicted for new/unseen data (X).
  * __Unsupervised__: In unsupervised learning, there is no label or target attribute. A typical example would be clustering data based on learned patterns. Like for a dataset of house details (area, location, price, # of bedrooms, # of floors, built date, etc.) the algorithm needs to find if there is any hidden patterns. For example some houses are very expensive while some others are of usual price. Some houses are very big while some houses are of usual size. With these patterns, records/data is clustered into groups like Luxury-Homes, Non-Luxury Homes, Bunglows, Apartment, etc.
  * __Reinforcement__: In Reinforcement Learning, an 'Agent' acts in an 'Environment' and receives positive or negative feedback. Positive feedback tells an agent that it has done well, and agent proceeds on similar plan/action. Negative feedback tells an agent that it has done something wrong, and should change it's course of action. The agent and the environment are software/programmed implementations. The core of reinforcement learning is building an agent (or agent's behaviour in some way) that learns to successfully accomplish a specific task in an environment.
* __Popular Algorithms__: [Linear Regression](https://en.wikipedia.org/wiki/Linear_regression), [Logistic Regression](https://en.wikipedia.org/wiki/Logistic_regression), [Support Vector Machines](https://en.wikipedia.org/wiki/Support_vector_machine), [K-Nearest-Neighbors](https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm), [Decision Trees](https://en.wikipedia.org/wiki/Decision_tree), [Random Forest](https://en.wikipedia.org/wiki/Random_forest), [Gradient Boosting](https://en.wikipedia.org/wiki/Gradient_boosting), [Ensemble Learning](https://en.wikipedia.org/wiki/Ensemble_learning)
* __Preprocessing__: In real world scenario data is rarely clean and neat in a state that Machine Learning algorithms can be directly applied on. Preprocessing is a process of cleaning data to feed to machine learning algorithm. Some of the common preprocessing steps are...
  * __Missing Value__: When some of the values are missing, they are usually dealt by adding median/mean values or deleting corresponding row, or using the value from the previous row, etc. There are many ways of doing this. What exactly needs to be done depends on the kind of data, problem being solved and business goals. 
  * __Categorical Variables__: Discrete finite set of values. Like 'car type', 'department', etc. These values are converted either into numbers or vectors. Conversion to vectors is known as [One-Hot](https://en.wikipedia.org/wiki/One-hot) Encoding. There are numerous ways of doing this in python. Some machine learning algorithms/libraries themselves handle categorical columns by encoding internally. One way of encoding is using [sklearn.preprocessing.OneHotEncoder](http://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.OneHotEncoder.html) in scikit-learn.
  * __Scaling__: Proportionately reducing values in columns into a common scale like 0 to 1. Having values in all columns in a common range might improve accuracy and training speed to some extent.
  * __Text__: Text needs to be processed using Natural Language Processing techniques (out of scope of this guide), when it isn't preprocessed, it is usually excluded from the training data that is fed to a machine learning algorithm.
  * __Imbalanced datasets__: The data shouldn't be biased, skewed. For e.g., consider a classification task where an algorithm classifies data into 3 different classes - A, B and C. If the dataset has very few/high records of one class w.r.t. others it is said to be biased/imbalanced. Usually data is oversampled in such cases by synthetically generating more random data from existing data.
  * __Outliers__: Outliers need to be dealt with on a case by case basis based on the problem and business case.
* __Data Transformation__: When a column/attribute in a dataset doesn't have an inherent pattern, it is transformed into something like log(values), sqrt(values), etc. where the transformed values might have interesting pattern/uniformity that can be learned. This is again, obviously case by case basis and needs data exploration to find a right fit.
* __Feature Engineering__: Feature Engineering is a process of deriving hidden insights from existing data. Consider a housing price prediction dataset which has columns 'plot-width', 'plot-length', 'number of bedrooms' and 'price'. Here we see a key attribute area of the house is missing, but can be calculated based on 'plot-width' and 'plot-length'. So a calculated column, 'area' is added to the dataset. This is known as feature engineering. Feature Engineering might be of different difficulty level, sometimes a derived attribute is right in front of sight like here, sometimes it's really hidden and needs lot of thinking.
* __Training__: This is a main step where the machine learning algorithm is trained on the given data to find generalized patterns to be applied on unseen data. Below are some important nitty-gritty details of this phase...
  * __Feature Selection__: Not all features/columns contribute to the learning. These are the columns where the data in them don't affect the outcome. Such features are removed from the dataset. What features to train on and what features to exclude is decided based on feature importance given by a machine learning algorithm being applied. Most of the modern algorithms do provide the feature importances. If an algorithm doesn't provide, scikit-learn or sklearn has utility functions which help find the feature importance. Also correlated features are removed.
  * __Evaluation Metric__: Evaluation metric is a metric used to evaluate predictions for their correctness. A machine learning algorithm while training uses an evaluation metric to evaluate, compute cost and optimize on the cost convex function. Though each algorithm has a default evaluation metric, it is recommended to specify the exact evaluation metric as per the business case/problem. Like some problems can afford false positives, but cannot afford any false negatives. By specifying the evaluation metric, these nitty gritty details of the model can be controlled.
  * __Parameter tuning__: Though most of the today's state of the art algorithms have sensible default values for the parameters, it always helps to tune the parameters to control the accuracy of a model and improve overall predictions. Parameter tuning can be done on a trial and error basis by repeatedly changing and assessing the accuracy. Alternatively a set of parameter values can be provided to try all/different permutations of those parameters and find the best parameter combination. This can be done using some helper functions called [Hyper-parameter Optimizers in scikit-learn](http://scikit-learn.org/stable/modules/classes.html#hyper-parameter-optimizers).
  * __Overfitting (Bias)__: Overfitting is a state where the machine learning model almost memorizes all the training data and predicts almost accurately on data that's already in training set. This is a state where the model fails to generalize and predict on unseen data. This is also known as model having high bias. Overfitting can be dealt with using Regularization, tuning hyperparameters if configured inappropriately, holding off partial dataset to use correct cross validation[(1)](http://scikit-learn.org/stable/modules/cross_validation.html)[(2)](https://en.wikipedia.org/wiki/Cross-validation_(statistics)) strategy.
  * __Underfitting (Variance)__: Underfitting is a state where the machine learning model's predictions don't do well even when predicting on data already in the training set. This is also known as model having high variance. Underfitting can be dealt with adding more data, adding/removing features, trying different machine learning algorithm, etc.
  * __Bias and Variance trade-off (sweet spot)__: The goal of model training is to find a sweet spot where the model cross validation error is minimum. Initially both cross validation and train error are high (Underfitting/high variance). As the model is training, the error keeps dropping to a certain point where cross validation is minimum and also close to train error (sweet spot). This is optimal spot. After this point, if the model further keeps reducing error (on train set), it almost memorizes the train set ends up overfitting which means higher error on unseen data.
  * __Regularization__: At some point when the model is trying to learn further (reducing error, tending towards overfitting), regularization helps in countering the overfitting effects. Regularization is usually a parameter that's added during cost/error calculation. Machine learning algorithms may not always provide regularization parameter explictly. In such case, usually there are other parameters that can be tuned to introduce regularization to the extent required.
* __Prediction__: To make predictions with trained machine learning model, the prediction method of the model is called by providing the test dataset as parameter. The test dataset should be preprocessed exactly the way it was done on the training dataset. In other words, in the same format of training data which was fed to the machine learning model for training.
* __Other terminologies__:
  * __Model Stacking__: When single machine learning algorithm doesn't do well, multiple machine learning algorithms are used to make predictions and the predictions are combined together in different ways. Most simplest being a weighted predictions. Sometimes, other machine learning model (meta-model) is used on top of the predictions of the first level models. This could go to any level of complexity and can have different pipelines.

### Deep Learning
Fun fact is that a majority (over 90% I guess) of all the machine learning problems solved today are solved using just Random Forests, Gradient Boosted Decision Trees, SVM, KNN, Linear Regression, Logistic Regression.

But, there are some set of problems that cannot be solved using above techniques. Problems like image classification, image recognition, natural language processing, audio processing, etc. are solved using a technique called Deep Learning. Before starting deep learning, I believe it's essential to master all of the above concepts first. 

Good Deep Learning resources...
* [Fast.ai](http://www.fast.ai/) -- thanks for the suggestion [Pranay Tiwari](https://www.linkedin.com/in/pranay-tiwari-47a49048/)!
* [neuralnetworksanddeeplearning.com - an online book, stresses on theory and fundamentals](http://neuralnetworksanddeeplearning.com/)
* [Deep Learning Specialization at Coursera by Andrew Ng](https://www.coursera.org/specializations/deep-learning)
* [deeplearningbook.org - an online book](http://www.deeplearningbook.org/)

If you know deep learning concepts and want to get your hands dirty, some popular Deep Learning Libraries are: [Keras](https://keras.io/), [CNTK](https://github.com/Microsoft/CNTK), [Tensorflow](https://github.com/tensorflow/tensorflow), [tflearn](https://github.com/tflearn/tflearn), [sonnet](https://github.com/deepmind/sonnet), [pytorch](https://github.com/pytorch/pytorch), [caffe](https://github.com/BVLC/caffe), [Theano](https://github.com/Theano/Theano)

### Practice
Yes, practice is the most important thing and this guide would have been incomplete without mentioning about practicing machine learning. To practice and master your skills further, below are the things you can do...
  1. Get datasets from various online data sources. One such popular data source is [UCI Machine Learning Repository](archive.ics.uci.edu/ml/). Additionally, you can [search 'datasets for machine learning'](http://google.com/search?q=datasets+for+machine+learning).
  2. Participate in online machine learning/data science hackathons. Some of the popular ones are - [Kaggle](http://kaggle.com), [HackerEarth](http://www.hackerearth.com), etc. If you end up starting with something that's very difficult, try persisting a bit. If it still feels difficult, park it aside and find other. There's no need to be disappointed. Usually problems on online hackathon have some level of difficulty which may not always be suitable for beginners.
  3. Blog about what you learn! It'll help you solidify your understanding and thoughts about the subject.
  4. Follow Data Science, Machine Learning topics on Quora, lot of great advice and questions/answers to learn from.
  5. Start listening to podcasts (available on link below)
  6. Check out some useful links on my [Data Science Learning Resources](http://abhijitannaldas.com/useful-stuff/) page.

### Closing thoughts
If you are considering the field of Machine Learning/Data Science seriously and you are thinking of making a career switch, think about the your motivations and why you'd like to do it.

If you are sure, I have one advice for you. **_Never ever ever give up or think if its all worth it_**. It's definitely worth it and I can say that as I have walked that path since last 18 months... almost every day, every weekend and every spare hour of my time (except when I was travelling or I was totally drowned by my day job commitments). The road ahead to master data science isn't easy. As they say, _"Rome was not built in a day!"_. You'll need to learn lot of subjects. Juggle between different learning priorities. Even after learning a lot you'll still find new things that you have never thought/heard about before. New concepts/techniques that you keep discovering might make you feel that you still don't know a lot of things and there is a lot more ground to cover. This is common. Just stick with it. Set big goals, plan for small tasks and just focus on task at hand. If something new comes up, just scribble it down in your diary and get back to it later.

### Thank You!
If you have been reading all the way till here, I appreciate your effort and the time you have invested. I hope this guide was useful to you and has made it little easier for you to get started on your own learning adventure. At some later point of time, if you think this guide has made some difference in your learning adventure, please please come back and leave a comment here. Or reach me at avannaldas .at. hotmail .dot. com. I'd love to hear from you. It'll give me immense satisfaction to know that this has helped you, and my effort in putting this together was worthwhile.

This was my biggest write up ever. I have spent many hours writing, editing and reviewing this. If you see any mistakes or things that can be improved, please let me know in comments or via email. I'll fix it the earliest I can and will attribute it to you. This will help everyone who reads this. 

Thanks Again!

All the best!
