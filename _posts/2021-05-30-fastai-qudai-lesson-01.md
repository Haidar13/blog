---
toc: false
layout: post
hide: false
search_exclude: false
comments: true
description: Answers to Fastai questionnaire in chapter 01
categories: [fastai]
title: Fastai lesson 01 Questionnaire
---


**1- Do you need these for deep learning?**

|Do you need?|T/F|
|---|---|
|Lots of math| T / ***F***|
|Lots of data| T / ***F***|
|Lots of expensive computers| T / ***F***|
|A PhD |T / ***F***|


**2- Name five areas where deep learning is now the best in the world.**

- Computer vision
- Medicine
- Biology
- Natural Language processing
- Recommender systems

**3- What was the name of the first device that was based on the principle of the artificial neuron?**

The Mark I Perceptron.

**4- Based on the book of the same name, what are the requirements for parallel distributed processing (PDP)?**

The PDP has 8 requirements: 

- A set of processing units
- A state of activation
- An output function for each of the units
- A pattern of connectivity between the units
- A propagation rule to propagate the activities patterns through the network connections
- An activation rule to combine the inputs in the unit with the current state of the unit to produce an output
- A learning rule to modify the patterns of connectivity based on experience
- An environment for the system to operate.

**5- What were the two theoretical misunderstandings that held back the field of neural networks?**

The first issue is that a single layer cannot represent some functions like XOR but adding a second layer will help, people only consider the first half of this statement. 

The second issue: In theory adding a second layer can approximate any mathematical function but in practice they are too big and too slow to train.

**6- What is a GPU?**

It is a specialized processing unit that was intended to process and display images and videos then later it was repurposed to perform neural network computation because it handles multiple tasks in parallel which is present in most of the neural network operation 

**7- Open a notebook and execute a cell containing: 1+1. What happens?**

The output *2* is printed in an output cell

**8- Follow through each cell of the stripped version of the notebook for this chapter. Before executing each cell, guess what will happen.**

*Done*

**9- Complete the Jupyter Notebook online appendix.**

*Done*

**10- Why is it hard to use a traditional computer program to recognize images in a photo?**

You need to manually write a lot of rules that might not be inclusive of all features that can be used to distinguish an image from the other

**11- What did Samuel mean by "weight assignment"?**

It means choosing a particular values for the program/model parameters that will improve the results

**12- What term do we normally use in deep learning for what Samuel called "weights"?**

The parameters

**13- Draw a picture that summarizes Samuel's view of a machine learning model.**

![]({{ site.baseurl }}/images/20210530-samual-model.PNG)

**14- Why is it hard to understand why a deep learning model makes a particular prediction?**

Because of the large interdependencies between the parameters that lead to a decision which makes it hard to pinpoint a single factor or set of factors that lead to the final decision.

**15- What is the name of the theorem that shows that a neural network can solve any mathematical problem to any level of accuracy?**

The universal approximation theorem.

**16- What do you need in order to train a model?**

- Input data
- Labels (can be annotated by humans or automatically generated from the data for example with auto-encoders)
- Loss function that can be used to compare the labels and the model output and how similar they are
- A method to update the weights or parameter values; the most commonly used method is back-propagation.

**17- How could a feedback loop impact the rollout of a predictive policing model?**

The bias and prejudice of the data and the way models are designed will produced biased output and it will be accurate with regards to the input biased data; when the model is deployed, it will reinforce the bias in the communities used to produce the initial data. The updated data according to the system output if used to update the model will still be biased.

**18- Do we always have to use 224×224-pixel images with the cat recognition model?**

No, the early models used this aspect ratio and it stuck with many pre-trained models. Depending in the the type of layer between the last convolution/polling layer of the network and the fully connected layers it might be possible to use a different image size even if the model was trained with 224x224 image size.

**19- What is the difference between classification and regression?**

In classification the final output or label is discrete (categorical) whereas the regression output is continuos. 

**20- What is a validation set? What is a test set? Why do we need them?**

Validation set is typically used to fine tune the hyper-parameters of the model; i.e. change the way we train the model or the size of the model then train on the training set the preform a test on the validation set after finishing the training we select the model based on the best performance on the validation set. The test set is not touched during the training or fine-tuning, it is only used after finalizing the model to check how it might perform on real world in unseen data.

**21- What will fastai do if you don't provide a validation set?**

Fastai will split the data randomly into 80% training and 20% testing subsets

**22- Can we always use a random sample for a validation set? Why or why not?**

No, for example if we have time series or time dependent data we cannot randomly select data from the middle of the series 

**23- What is overfitting? Provide an example.**

Overfitting occurs when the model memorizes the training data and does not generalize to unseen data. for example a voice to text model that can only transcribe a voice that has been used in the training and any slight modification to the voice can cripple the system.

**24- What is a metric? How does it differ from "loss"?**

The loss is used to adjust the model parameters and it measure how close the training labels to the predicted labels. The metric on the other hand, is related to the problem that we are trying to solve for example in classification problem it can be the accuracy or F1 score, in segmentation it can be dice or intersection over union score, for regression problem we can use the mean square error

**25- How can pretrained models help?**

Pre-trained models learn the low level features that are common in many tasks this can help is in fine-tuning the models by updating the parameters used for the high-level features at hand which can reduce the training time and the amount of data needed

**26- What is the "head" of a model?**

The head of the model is the last couple of layers of a neural network that are usually trained during fine-tuning

**27- What kinds of features do the early layers of a CNN find? How about the later layers?**

Early layers find low level features such as lines and edges. Later layers try to find high level features like eyes and mouth in case of face detection.

**28- Are image models only useful for photos?**

No, it can be used in other modalities for example 1D sound signal can be converted into 2D spectrogram then used as input to image models.

**29- What is an "architecture"?**

It is the number of layers, the type of layers, the order of the layers, and the interconnection between them.

**30- What is segmentation?**

Assigning a class to each pixel in the image, each class can represent a type of object.

**31- What is `y_range` used for? When do we need it?**

It is used to scale the output of the network sigmoid layer

**32- What are "hyperparameters"?**

They are parameters the are typically used during the training of the model to control how the model is being trained but not used in the final trained model for inference. 

**33- What's the best way to avoid failures when using AI in an organization?**

First make sure the problem at hand is clearly defined and that it needs AI and the upper management support the project, then collect a valid dataset for training. After collecting the dataset try different models and ways of addressing the problem and split your data into training/validation/testing to make sure the model is robust. After deploying the model make sure to update it regularly to avoid the data distribution shift and the organizational priorities and operations shift.