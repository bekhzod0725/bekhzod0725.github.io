---
layout: post
title:  Titanic and Neural Networks
date:   2016-09-28 00:05:15 -0400
comments: true
published: false
categories: dnn rnn cnn neural networks data analysis kaggle python tensorflow skflow scikit numpy
---

I recently opened an account on [Kaggle](https://kaggle.com). I knew about Kaggle for a while, however never had a chance to use it. 
Now that I am getting involved with data analysis more, I have to tell ya, I love it. It's probably the best place to actually learn and test your data skills.


Alright, enough talk. Let's get back to business.

#Intro
##Titanic
Probably one of the most, if not the most popuplar tasks on Kaggle is "Titanic: Machine Learning from Disaster". As it is said on the task's main page, this is the best place to start on Kaggle. There are more than 5000 people competing on the leaderboard. However, I couldn't find one thing. No one ever done any Neural Network analysis on this particular topic, or even if some one had done it they never published it. Therefore, I wanted to add my 50 cents to this area.

##Neural Networks
I have to tell you from the beginning: using Neural Networks in this assignment will not do any good. Cause NN simply doesn't work for this dataset. Why? Because of the lack of data. Neural Networks need tons of data to be accurate in their results. However, the Titanic dataset contains only 891 rows of training data.You simply cannot train a good neural network that will predict the test data 100% with this amount of data. But, I will do my best to walk you through of the process how Neural Network solutions could be implemented for this specific dataset.

#Process

