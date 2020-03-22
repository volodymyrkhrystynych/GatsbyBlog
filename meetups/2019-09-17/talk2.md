# Dimensionality reduction in healthcare
## Ali from UofT

Works with predicting cancer survival and reaction to drugs

Works at Cyclica

health data comes from patients, animals, and cell lines

You can get information from medical records, imaging, molecular features, features in moelcules

issue is the dimensionality, you could have just a few hundred patients, a few hundred thousand molecular features and so on.

when you talk about the dimensionality reduction you cannot talk about the density of your clusters, nor you can you talk about the distance between the clusters, nor can you use it to disprove or prove a hypothesis

Dimensionality reduction
PCA - principal component analysis
t-SNE - t-Distributed stochastic neighbor embedding
UMAP - Uniforom Manifold approximation and projection

If you get really nice clean pca seperation for medical it could be a technology effect, if you have data from 2 hospitals and one of them has consistently incorrectly imputed data.

umap is a very good dimensionaly reduction

t-SNE has a hyperparam called perplexity that can generate nice clusters from random data, and thus be careful of use
