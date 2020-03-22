# Deep learning for self driving at uber ATG R&D lab

Self driving is incredibly complex

Car needs to understand what is around it

sensors > perception > prediction > motion planning > controls

AVMaps & Localization
Framework
Computing

motion planning : how can i do what i want keeping with all the
regulations(user comfort, traffic laws)

Cloud latency unacceptable

End-to-end learning
Simple easy to train
Hard to interpret
Uncertainty propogated
Optimize for task at hand
Hard to incorporate
Labelled data is driving
Shared computation -> fast

Traditional engineering
Pipelined syste, is messy and overtune dependencies
Interpretable intermediate steps
Hard decisions (uncertainty is not propogated)
Are we optimizing for the right probble,
Can incorporate prior knowledge easily
Hard to get labelled data
Separate computation -> slow

Goal:  End to end learnable interpretable driving system

Combined perception and prediction

Want to predict lane changes, stopping, more complex actions.

they have a module that specifically detects turn signal use

Combining lidar and image data is hard

ResEng - Research > production
 - Data wrangling
 - runtime/perf optimization
 - prpduction training
 - inference integration
 - Compute/storage DL infrastructure
 - Metrics & Testing

Answer:
Road work is difficult and is generally considered a seperate
problem
Autonomous cars cannot break traffic laws and that makes certain
situations difficult.
The car keeps several seconds of memory for prediction.
There is an entire team/dep in Uber self driving for safety.
There is a subsystem designed for collision avoidance that can
override the main system.
There is a hell of a lot of testing before a piece of code goes
into a car on the road.
What do you communicate when multicar integration is done?

