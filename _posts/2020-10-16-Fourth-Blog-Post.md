---
layout: post
title: Project 2
---

# Project 1: News Data
## Data Setup
The overall goal of the Mashable data set was to collect information on their articles and then identify anything that could predict the number of shares.
For our project we wanted to find predictions for each day of the week.
To get this started I first filter the data for the desired week day. I then create test and train data sets to prepare for our modeling!

## Data Exploration
Before we can start modeling we have to exlpore the data a bit. 
I started off by looking at the summary statistics of each variable. Nothing really stood out to me!
Next I wanted to take a look at the correlations! I first look at the correlations between shares and the rest of the variables.
I decided to focus on the variables that were more highly correlated with our response variable.
I also took a look at the rest of the correlations to be sure I avoided any combinations of variables that were highly correlated. This is particularly important with this data set because many of the variables overlap and are in fact related.
Lastly I created some plots! 
I took a few variables that stood out and plotted them agains the response variable. Unfortunately I didn't find any patterns that really stood out.
I also plotted histograms for all of the variables, again I didn't really see anything very notable. 

## Modeling 
When choosing models I did a combination of variables that would make sense logically to affect the number of shares (word counts, image counts, video counts, etc...) and those with the higher correlations I found from my data explorations.
We wanted to fit a classification tree model using the leave on out cross validation and a boosted tree model using cross validation. I tried to fit 3 models for each method and chose fits with the smallest RMSE.
With a fitted model for each method I then wanted to compare the predictions to the test data. Of course our models weren't that great, but I then calculated the RMSE to evaluate which method had the better fit.

Check out my project!
[My Repo Link For Project1](https://apolanc2.github.io/Project2/)
