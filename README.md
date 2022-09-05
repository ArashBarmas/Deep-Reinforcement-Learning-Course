
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

The goal in policy based methods is to maximize $U(\theta) = \sum_{\tau} p(\tau ; \theta) R(\tau)$

Taking the derivative w.r.t to $\theta$ along side with some math tricks give us: 

$\nabla_{\theta} U(\theta) = \sum_{\tau} p(\tau ; \theta) \nabla_{\theta}log(p(\tau ; \theta)) R(\tau)$

$\nabla_{\theta} U(\theta) = \frac{1}{m} \sum_{i=1}^{m}\nabla_{\theta}log(p(\tau ; \theta)) R(\tau)$

$\nabla_{\theta} log(p(\tau^{(i)}; \theta)) = \sum_{t = 0}^{H} \nabla log \pi_{\theta}(a_{t}^{(i)} | s_{t}^{(i)})$


This can be used no matter what our reward function is; we don't need a derivative of the reward.

After collecting trajectories, we can estimmate the gradient using $\nabla_{\theta} U(\theta)$. Then, SGD to update theta. We can utilize the pytorch .backward() function to compute the gradient. 


#### 4. Proximal Policy Optimization (PPO):

Reinforce has some drawbacks such as inefficient update process, noisy gradient estimation, and lack of credit assignment.


1. Reward Normalization: normalize rewards to imporve learning by making sure the steps of the gradient aren't too large or too small.

2. Assign Credit: assign credit to action a by multiplying to the future reward in gradient calculation.


















