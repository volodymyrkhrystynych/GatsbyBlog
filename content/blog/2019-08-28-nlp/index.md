# NLP feature engineering

## Hands on feature engineering
Susan Li from Kognitiv

Feature engineering for nlp
TF-IDF
 - count the number token that contain a certain work then multiply that by (total docs/docs that contain the word)
 - you compute this for each token you are searching over
 - Allows you to use a feature vector as an input field
Word2vec
 - not deep learning
 - CBOW predicts the current word given the neighbouring words
 - Skip-gram does the opposite
FastText
 - can generate better embedding than word2vec
 - can construct a result even if word was not in training
 - gensim library
Topic Modelling
 - this is an unsupervised learning algorithm
 - use intertopic distance map to see is your topics overlap
 - not all topics can be defined well
 - useful for data exploration
 - inconsistant data can fool the system, if two hotels have the same poor description of check-in time and whatnot then this technique would assume that they are similar.

The future might look like automatic feature engineering
How does one explain end to end feature engineering and how do you debug it with it breaks?
Good feature engineering are the backbone of machine learning
Feature engineering for machine learning book O'Reilly

If you have several labels that are so similar that even a human would have trouble correctly labelling them it might be a good idea to consolide the labels
:research:
Stackoverflow tensorflow workshop examples
problem is that all questions only have one tag in this dataset

fuzzywuzzy
gensim

### model explain ability pythom projects
Lime
Shap

## Understanding predictions: Machine learning interpretability
Pratap Rumamurthy from H20

ml pipeline:
data integration & quality
feature engineering
model training
machine learning interpretability

white box and black box models

why explain?
multiplicity of good models
fairness and social aspects
trust of model producers and consumers
security and hacking
regulated/controlled environments

## Surrogate Model
you can create a surrogate model that is explainable using your model to create a new dataset in order to have your surrogate to converge to your main model

if you need perfect interpretability to a complex model you can create a surrogate interpretable model around a specific point, it will be explainable around that point only.

Eg:if you have a model predicting something using profile information you can make everything static and just change age in order to understand what it is doing.

## feature ranking based on permutation

take one feature, shuffle the values and predict again, the drop in accuracy of your original model will imply how important that feature is.




