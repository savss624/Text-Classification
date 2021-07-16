# 20 Newsgroups Classification

## Text Classification
Text classification or Text Categorization is the activity of labeling natural language texts with relevant categories from a predefined set. In laymen terms, text classification is a process of extracting generic tags from unstructured text. These generic tags come from a set of pre-defined categories. Classifying your content and products into categories help users to easily search and navigate within website or application.

## Approach - NAIVE BAYES
There are three types of Naive Bayes models under the scikit-learn library:
* Gaussian
* Multinomial
* Bernoulli

Here, I'm using Multinomial NaiveBayes which is quite powerful and fast when it comes to text classification.
### But What is Multinomial Naive Bayes? 
It is used for discrete counts. In laymen terms, it count how often word occurs in the document, you can think of it as “number of times outcome number 𝑥𝑖 is observed over the n trials”.

## Data - [20 Newsgroups](http://archive.ics.uci.edu/ml/datasets/Twenty+Newsgroups)
The 20 Newsgroups data set is a collection of approximately 20,000 newsgroup documents, partitioned (nearly) evenly across 20 different newsgroups.

First, we need to transform the dataset articles into a proper format that can be consumed by a NaiveBayes model. And the technique that we're gonna use to preprocess the data is called ***Bag of Words***.
### ***"Bag of Words"*** includes few steps:
* Tokenization: Get tokens from all articles
* Dictionary Making: Count all tokens
* Feature Preparation: Extracting top few thousand tokens possessing the maximum frequency
* DataFrame Making: Making Dataframe with tokens as columns, articles as rows & the token count in that article as values

## Modeling
Next and the most important step, model making.
### Fit Function: 
Here, we will make a dictionary with model classes as keys, a new dictionary as its value & this dictionary has model features as keys and its count in the training data of class(key of parent dictionary).
