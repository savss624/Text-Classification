# 20 Newsgroups Text Classification 

![intro image](https://lionbridge.ai/wp-content/uploads/2019/12/2019-12-11_14-best-text-classification.jpg)
## Text Classification
Text classification or Text Categorization is the activity of labeling natural language texts with relevant categories from a predefined set. In laymen terms, text classification is a process of extracting generic tags from unstructured text. These generic tags come from a set of pre-defined categories. Classifying your content and products into categories help users to easily search and navigate within website or application.

## Approach - NAIVE BAYES
NaiveBayes works on Bayes Theorem

![bayes theorem](https://github.com/savss624/Readme-Images/blob/main/20NewsGroup/bayes.png)

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
Fit Function prepares a dictionary with model classes as keys, a new dictionary as its value & this dictionary has model features as keys and its count in the training data of class(key of parent dictionary).

### Predict Function:
The Predict Functions calculates the probability of all the classes for an article using Bayes Theorem and Laplace Correction, then predict the class which possess the maximum.

Now, we have the processed data & the model. So
## Let's make some predictions
On testing the 25% of the original data, Our model gave us some pretty accurate predictions.
Let's have a look at model stats:

![model stats](https://github.com/savss624/Readme-Images/blob/main/20NewsGroup/stats.png)

Our Classification Model actually works. We achieved **86%** accuracy.

## Additional Info
Naive Bayes classifiers mostly used in text classification (due to better result in multi class problems and independence rule) have higher success rate as compared to other algorithms. As a result, it is widely used in Spam filtering (identify spam e-mail) and Sentiment Analysis (in social media analysis, to identify positive and negative customer sentiments)
