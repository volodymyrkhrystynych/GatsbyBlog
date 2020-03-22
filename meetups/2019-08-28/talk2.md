#Understanding predictions: Machine learning interpretability
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


