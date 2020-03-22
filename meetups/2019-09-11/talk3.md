# Pareto-Optimal Embedded modeling: discarding information to predict drug properties
## Andrew Brereton

Predicting ADMET
 - Absorption
 - Distribution
 - Metabolism
 - Excretion
 - Toxicity

How do you get a molecular structure to be useful to a computer?

There is a problem with sparse data when you have the need to be able to encode small and large molecules?

POEM method

Using tanimoto similarity to use all molecule fingerprints at the same time.

take N molecule fingerprints and calculate the tanimoto similarity for each and you get an N length vector.

You can then use this vector to calculate the similatiries between different molecules and rank them based on similatiry.

POEM is an improvement compared to similar models.

advantages is that it is not a black box
disadvantage is that due to the pair comparison it can be computationaly expensive in large datasets and the mix of your comparison molecules can really impare your predictions.
