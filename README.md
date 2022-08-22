# Deep-Reinforcement-Learning-Course
Deep Reinforcement Learning Course


# U-DRL:


## Policy Based Methods Tutorials:

#### 1. Cross Entropy Method: 

Train an agent using OpenAI Gym's MountainCarContinuous environment with a Cross Entropy optimization which iteratively suggests a small number of neighboring policies(weights), and uses a small percentage 
of the best performing policies to calculate a new estimate.

#### 2. Hill Climbing: 

Train an agent using OpenAI Gym's Cartpole environment with a Hill Climbing optimization which iteratively purturbs the values of the current best estimate of weights and use those weights if it yields higher return.


#### 3. Reinforce:
  
Train an agent using OpenAI Gym's Cartpole environment with the REINFORCE algorithm.

REINFORCE:

  i) use the current policy to collect m trajectories
  
  ii) use the trajectories to estimate gradient of E[R(t(w))]
  
  iii) update the weights w <- w + alpha*gradient
  
  iv) loop over i-iii












