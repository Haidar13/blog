---
toc: false
layout: post
hide: false
search_exclude: true
comments: true
description: Exercises solution for Session 1.
categories: [D2LSG]
title: D2L Study Group Session 1 Exercises
---

## Exercises from d2l.ai first chapter

**1. Which parts of code that you are currently writing could be “learned”, i.e., improved by learning and automatically determining design choices that are made in your code? Does your code include heuristic design choices?**

 I am working on image classification code, most of the work is done using learning. There are however some parts that need some heuristic choices for example the hyperparameter of the model, the model architecture, and the workflow of the entire process. For some of these tasks, an active research is being done like model selection and hyperparameter tuning with tools such as AutoML.

**2. Which problems that you encounter have many examples for how to solve them, yet no specific way to automate them? These may be prime candidates for using deep learning.**

 Sorting good from bad produce before taking them to market.

**3. Viewing the development of artificial intelligence as a new industrial revolution, what is the relationship between algorithms and data? Is it similar to steam engines and coal (what is the fundamental difference)?**

 There are some similarities and some differences between the two. The coal is the source of the engine power without it the engine could not move, similarly, the data powers the artificial intelligence systems. One main difference is the quality of the raw material and its effect on the end result. A good quality coal is better but the consequences of bad quality coal is not the same as bad quality data. The bad coal will probably reduce the efficiency of the engine but adding more of it can balance out the performance. In artificial intelligence, in the other hand, adding more bad data will cripple the performance of the system and can lead to dire  consequences like misdiagnosis or bias policing.

**4. Where else can you apply the end-to-end training approach? Physics? Engineering? Econometrics?**

 End-to-end training can be applied in many scenarios. For example in medical image analysis, astronomy, remote sensing applications and many more. There have been a lot of examples:

 1. Zeyer, A., Irie, K., Schlüter, R., & Ney, H. (2018). Improved training of end-to-end attention models for speech recognition. arXiv preprint arXiv:1805.03294.‏

 2. Kokkinos, I. (2017). Ubernet: Training a universal convolutional neural network for low-, mid-, and high-level vision using diverse datasets and limited memory. In Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (pp. 6129-6138).‏

 3. de Vos, B. D., Berendsen, F. F., Viergever, M. A., Staring, M., & Išgum, I. (2017). End-to-end unsupervised deformable image registration with a convolutional neural network. In Deep Learning in Medical Image Analysis and Multimodal Learning for Clinical Decision Support (pp. 204-212). Springer, Cham.‏

And many more

## One page summary of Chapter 1

### **Introduction**

Until recently most programs relay on developer going through all corner cases possible and writing code to deal with it. But there are some problems that we cannot deal with using this method. For example, prediction the weather, identifying people in photos, or product recommendations.
This can be due to different reasons for example the relationship between the pixels and the abstract category is very complex.

Machine learning is a set powerful techniques that learns from observing a large amount of data.

### **Motivation example and the learning process**

The authors gave an example of how to recognize the voice prompt for digital assistance like Alexa or Siri the learning process has the following steps:

1. Start off with a randomly initialized model that cannot do anything useful.

2. Grab some of your labeled data.

3. Tweak the knobs so the model sucks less with respect to those examples.

4. Repeat until the model is awesome.

Deep models are deep in precisely the sense that they learn many layers of computation

### **The Key Components of Machine learning**

Machine learning consists of the following main components:

1. Data
   Generally, we are concerned with a collection of examples (also called data points), which typically consists of numerical attributes (or features), in supervised learning we also have target value. Generally the more data we have the better models we can build.

2. Model
   Models can be thought of as a computational machine that ingest data and spit output. In many cases we can thing of it as a statistical  model built from the data. Deep learning model is different from classical models by the powerful models it creates by doing multiple transformation of the data before getting the end result.

3. loss (objective) function
   The objective function as a formal measure of how good or bad our model is doing. For predicting a numerical output, a common objective function is squared error $(y-\hat y)^2$, for classification function we typically use the error rate.

4. Optimization Algorithm
   The optimization algorithm is an algorithm capable of searching for the best parameter of the model using the data and the loss function.

### **Kinds of Machine Learning**

1. Supervised learning
   Supervised learning addresses the task of predicting targets given inputs. The target (labels) are usually denoted by $y$ and the input features are denoted by $X$. The goal is to produce a model $f_\theta$ that takes input $X$ and produce output $y$ i.e. $f_\theta(X) \mapsto y$.

   Examples of this includes:

    * Predict cancer vs not cancer, given a CT image.

    * Predict the correct translation in French, given a sentence in English.

    * Predict the price of a stock next month based on this month’s financial reporting data.

    There are several types of supervised learning here is a list of them

    1.1 Regression

    In regression we try to predict a continues value for example a house price or a stock value.

    1.2 Classification

    In classification we try to predict a discrete value for example does this image have a tumor.

    1.3 Tagging

    Tagging is to predict classes that are not mutually exclusive also known as multi-label problems where an instance or data point can contain multiple labels or targets

    1.4 Search and ranking

    In addition to predicting if the set of instances contained the required information (or labels), the search and ranking algorithms rank the result by the most relevant instance. For example, when searching the web for pages containing the phrase "deep learning framework comparison" we need to get all pages related to this phrase but also rank them putting the most relevant ones at the top.

    1.5 Recommender systems

    The recommender systems has a similar objective as the search and rank problems with the addition of personalization. The results needs to be relevant to the individual users. For example recommending a movie or a product in an e-commerce website based on the previous selection of a particular user

    1.6 Sequence Learning

    There are some problems where the target cannot be predicted using simply a single instance, for example predicting the next word in a translation system needs to take into account the sequence of words that came before, or when predicting the patient outcome using the results from the last couple of visits and lab reports. Here sequence learning models can help.

2. Unsupervised learning

   The unsupervised learning approach does not use target labels, it only use the data or features and it tries to find patterns or it compact the data into a smaller dimension by extracting the most relevant information from each instance

3. Reinforcement learning
   In reinforcement learning, the model (or agent) is interacting with the environment, consuming data and producing actions that might change the environment or the agent state. In supervised and unsupervised learning the data is collected beforehand and the model interactive with offline data whereas the reinforcement learning agent observe the environment to collect data and act upon them.
