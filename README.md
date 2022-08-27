
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

The goal in policy based methods is to maximize the expected return or utility function. REINFORCE is a math trick to make the calculation easier.
We can also utilize the pytorch .backward() function to compute the gradient. Thus, we need just find the policy loss by looping over trajectories and 
summing up log output * reward.

I have more info in the reinforce file.













