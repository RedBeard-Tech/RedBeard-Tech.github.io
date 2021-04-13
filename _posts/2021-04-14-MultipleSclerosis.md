# Multiple Sclerosis, is inflammation the culprit?

Table of contents:

1. TOC
{:toc}

## Introduction

I wrote my master's degree in coorperation with NOFIMA, a leading research institute with offices in Norway. During this time I had the pleasure of working with my supervisor Ellen Mosleth, who at the time was writing the following [research paper](https://www.nature.com/articles/s41598-021-82388-w). If you clicked on the link and read the names of the co-authors you might have noticed that my name is listed as one of them. If you wish to find out why you can continue reading this post.  



## General backround information

What is MS?
- Include quotations from research paper
Why MS? 
What is the current understanding of MS?
What did the research paper linked do?
What are the different types of MS?
How many people get MS?
Medicine for MS?

Inflammation vs no inflammation. How is this significant wrt medicine?


## Aim

What is the aim of this blog/ your code
What is the motivation?
How is it significant?
What effects can the results possibly have?

## Dataset

Information about how the data was gathered and when
 - What is cerebral fluid test? 
 - What are protein markers and why are they significant?
 - What are the challenges of this dataset wrt our aim?
 - How can your readers (hopefully in the plural form) access the dataset?
 - Preprocessing done on the dataset?

## Methods

- What methods are you using to investigate or reach your aim?
- What is RFECV, PCA, different mahcine learning models?
- maybe link your master thesis for greater detail? 
- Weak links to your methods?

The following steps should be undertaken for a random target and a valid target to see if for a random target you can find features that differentiate the samples. If not then great this method actually finds structure in the underlying features separation MS and inflammation. 

Steps:
1) Split data into training and test set (This is a bit of a challenge since you only have 100 rows) IDK if you should do this
2) Choose the different algorithms to use (catboost, xgboost, randomforest,svc(linear) has to be an algorithm where you can measure feature importance
3) Use RFECV to fit the different models on training/whole dataset for finding optimum number of features for each model
4) Use a linear type of algorithm to fit the first 2 principal components of the extracted features on whole. If you are able to fit on whole after finding RFECV on training set only then this is a type of validation. You could also drop this step and just assess visually if PCA plot separates any good. 
5) Select the feature sets with the highest linear model fit

The weak side of these steps is that you cant validate your results. The only validation you sort of have is due to testing the steps on a random target and hopefully seeing bad results. If  good results are indicated then this method is obviously a bad one if you cant validate it.

## Code

How can you show your code?
- should you make a notebook or take snippits?


## Conclusions

What conclusions can you draw?
What conclusions did the research paper draw?
How did the method perform?


## Footnotes

I am not sure if I need a footnote... 

