#Practical Machine Learning Workshop
## Xiaozhou Wang (Quartic AI, kaggle grand master)
ranked #4 in the world on kaggle

Quartic does ai for manufacturing and industry

ML life cycle
problem definition > Data collections > Model training and optimization > QA & deployment

Not really linear, a very messy life cycle in reality

##Problem definition

Is it even doable with ML right now?
 - Are there any deployed applications or published papers on similar problems
 - Can we acquire enough data?
 - How costly is it to have a useful model (e.g. required computer/accuracy)

How much impact does it have?
What metric are you going to use?

The most important thing is having a good test set.
 - Is it representative of the reality?

Train a lightgbm model and check if AUC is around 0.5 on test set to check so that there is no pattern

Once you have a good test and validation set and a good metric you have everything necessary to start trying different models and comparing them.

## How to train and iterate?
 - Set up the baselines
	 - the lower bound : the simplest model
	 - "Good enough" Upper bound : human performance, data quality/label accuracy
 - take advantage of the off the shelf SoTAs (state of the art models)
	 - There really isn't a point in trying everything, find the best models for that specific application or something similar and try that
 - Balance the speed and accuracy while iterating
	 - Iterate quickly while doing the algorithm/hyperparameter search
		 - smaller training set?
		 - smaller image size?
 - Understand the uniqueness of the dataset
	 - Almost impossible to estimate how much improvement you are going to have after a fixed amount of time 
	 - It becomes exponentially harder to get a better model after each iteration
	 - It is more of an art and science
		 - feature engineering
		 - deep learning model architecture/hyperparameter selection
		 - data/problem specific ricks (e.g. preprocessing, post processing, etc.)
 - Try transfer Learning whenever you can
 - Team collaboration
	 - remove the test set from the data and give it to the manager or quality control so that it is the final test.
	 - See if the model can be reproduced from the training script by the final validator

fasttext embedding
wordtovec

SeResNext50
avg pooling image layers
Usually 2 layers is good enough when you have all numerical data (check yourself)


Execute it like a startup
 - Do things that dont scale
	 - just trhow things at the wall and see what sticks 
	 - jupyter notebook on local desktop
	 - hacky code
 - always go for the higher/quicker ROI (MVP stage)
	 - neet io iterate and deploy to see if it is actually impact full
 - build up the infrastructure
	 - make sure it is stable and can be more and more valuable
	 - unit + integrations tests

5 Gold medals on kaggle to become grandmaster
Do competitions that will teach you something
if you dont know how to do image processing do an image processing kaggle competition

usually 3-4 weeks learning the domain 30 hours when it is a know thing




