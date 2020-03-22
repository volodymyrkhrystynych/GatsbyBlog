# Elastic distributed deep learning training at large scale
## Yonggang Hu
## Tech champion in IBM, pioneer for IBM Watson
## on of the ai engineers at IBM (his description)

allreduce for sgd
this allows for data paralellism

The problem is that the slowest computer in your network determines your speed

Elastic training is allowing a model to train on some gpus and let that increase as availible and decrease if there is more demand without stopping training.

horovod allows this

Distributed tensorflow also allows this

second speaker for this talk gave a demo of elastic training, it works by waiting for the gpus to finish training the iteration and for the weight to be transfered between them before reallocating the gpus to new jobs.
 
 The program also allows for realtime viewing of accuracy for realtime understanding of whether your algorithm is getting anywhere.
 
 developer ibm dynamic resilient and elastic deep learning
