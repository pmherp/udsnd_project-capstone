# Sparkify-App: Prediction on User Churn

## Introduction
This is the Capstone Project of the Udacity Data Scientist Nanodegree programm.

Sparkify is a fictional music streaming platform created by Udacity. For this project we are given data from this platform in order to generate insights on user churn.

Udacity provides a mini, a medium and a large version of data. I have used the mini version of the data. Due to file size restrictions, none of the versions are provided together with the code.

## Motivation
For this project I will be looking at two months worth of data from a fictional music streaming app called Sparkify. That data contains basic information about the apps users as well as information about a single action. A unique user can have multiple entries based on interaction time and activity with the app itself. Churned users are distinguished from non churned users based on their interaction with the cancellation page.

The aim of this project is to create a robust model based on the given data which effectivly predicts wether a user will churn or not based on different features.

### Libraries and Code
The code should run smoothly using python 3.7* and above.

The code itself uses different libraries from Python and PySpark. These need to be installed on a local machine to get the code to work. This libraries include:
- pandas
- matplotlib
- seaborn
- sklearn
- gc (garbadge collector)
- pyspark.ml
- pyspark.sql
- pyspark version 3.0.2

### Data
For this project, there are different versions of datasets, which only differ in size. The files are not provided due to upload restirctions of github. If you want to run this project on a bigger dataset, the code will need to be adjusted to run on multiple machines.

- mini_sparkify_event_data.json: This is the file used for this project
- medium-sparkify-event-data.json.gz
- If you have an AWS account, a large dataset(12 GB) has been public on s3n://udacity-dsnd/sparkify/sparkify_event_data.json

### File Description
The main file of this project is "Sparkify.ipynb". This notebook holds all the code for this project as well as the entire structure of loading and exploring the data, feature engineering and machine learning.

## Overview
### I. Loading and Cleaning
In this workspace, the mini-dataset file is mini_sparkify_event_data.json. Load and clean the dataset, checking for invalid or missing data - for example, records without userids or sessionids.

### II. Exploratory Data Analysis
When you're working with the full dataset, perform EDA by loading a small subset of the data and doing basic manipulations within Spark. In this workspace, you are already provided a small subset of data you can explore.

Define Churn
Once you've done some preliminary analysis, create a column Churn to use as the label for your model. I suggest using the Cancellation Confirmation events to define your churn, which happen for both paid and free users. As a bonus task, you can also look into the Downgrade events.

Explore Data
Once you've defined churn, perform some exploratory data analysis to observe the behavior for users who stayed vs users who churned. You can start by exploring aggregates on these two groups of users, observing how much of a specific action they experienced per a certain time unit or number of songs played.

### III. Feature Engineering
Once you've familiarized yourself with the data, build out the features you find promising to train your model on. To work with the full dataset, you can follow the following steps.

Write a script to extract the necessary features from the smaller subset of data. Ensure that your script is scalable, using the best practices discussed in Lesson 3. Try your script on the full data set, debugging your script if necessary. If you are working in the classroom workspace, you can just extract features based on the small subset of data contained here. Be sure to transfer over this work to the larger dataset when you work on your Spark cluster.

### IV. Modelling and Evaluation
Split the full dataset into train, test, and validation sets. Test out several of the machine learning methods you learned. Evaluate the accuracy of the various models, tuning parameters as necessary. Determine your winning model based on test accuracy and report results on the validation set. Since the churned users are a fairly small subset, I suggest using F1 score as the metric to optimize.

## Results
A detailed review of the results can be found in this blogpost [here]() (not working yet).

## Reference
I want to give credit for the data provided by Udacity's Data Scientist Nanodegree course.