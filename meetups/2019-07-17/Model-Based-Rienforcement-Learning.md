#Model-Based reinforcement learning
##Katya Kudashkina
Cultura.ai - her startup
kk@cultura.ai
@KatyaKuda

predictive learning ~ unsupervised learning ~ model-based RL
learning models of the world
learning to reason and plan

markov decision process
world state > user action > world reward

Partially observed environment
- world state is unknown, observations are substitues

Markov state - all necessary info
Information state - minimal markov state
Environment stae - consists of info the env uses in determining
the rewareds
Agent state - info an agent uses to act

Policy pi is a probability distribution over all possible actions
a in A(S) at give state s

gamma = discount rate

value base methods - compute value functions
 - prediction-type
 - control-type
Policy based methods - directly optimize and compute the policy
pi

actor-critic combine value and policy based methods
actor produces policy
crity produces value

asside - Richard suttons book for gradient descent

State update function
 - an approximation
 - feature-vector
 - carries the history of the sequence
 - usefullness

#What is the purpose of the;model
 - The model looks ahead, imagining the future
 - generate simulated experience and can be used to fit the
   value functions of the policy better
 - provides information about features

Types :
 - Distribution models
	 - output : a distribution over state 
	 - not enough info
 - Sample models
	 - a sample state 
	 - its a sample
 - Expectation models
	 - an expectation state feature-vector
	 - some information lost

Closed quections in model-based RF
 - plannign should be online and incremental
 - models and planning should be state to state
 - sophisticated search control is essential
 - subproblems are essential

Open questions
 - state update function
 - how planning affects action selection
 - how update policy and value function
 - should the reward come from an environment
 - should model generate sample states of expected states
 - should we use average reward (no discounting)

Her focus is dialogue systems
 - wants to create a system that understands context

Why reinforcement learning for intelligent assistants?
 - rlformalizes the goal
 - formalization is interactive
 - is about learning
 - is online
 - is more general autonomous
 - can act and generate its own behavior
 - requires less explicit training feedback
 - the agent doesnt know what it shoud have done, but it know
   ifthe action taken was bad
   
MBRL
 - 70 times sample-efficiency
 - quick adaptability to a user
 - deployment of the lightweight models
	 - great succes in using the same ai with the model
	   removed after training.
	   
	   
	   
	   
