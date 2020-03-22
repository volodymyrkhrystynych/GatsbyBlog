# Introduction to the deep learning pipeline

 - Linear Transformation

 - Standardization
	 - get the mean of the data
	 - subtract the mean from every sample
	 - clusters the points around 0
 - Principle component analysis
 - then standardize (PCA(whiten=True))
 - If you do pca before test train split you might be giving the ml algorithm answers

