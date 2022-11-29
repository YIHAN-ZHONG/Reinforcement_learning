# Reinforcement learning
Introduction to RL models by discovering OpenAI GYM with an implementation of Value Iteration, Policy Iteration
and Q-learning. 

The environment implemented is Cliff Walking Environment (from Sutton's book).

    Adapted from Example 6.6 (page 132) from Reinforcement Learning: An Introduction
    by Sutton and Barto:
    The board is a 4x12 matrix, with (using Numpy matrix indexing):
        [3, 0] as the start at bottom-left
        [3, 11] as the goal at bottom-right
        [3, 1..10] as the cliff at bottom-center
    Each time step incurs -1 reward, and stepping into the cliff incurs -100 reward
    and a reset to the start. An episode terminates when the agent reaches the goal.

You can find the code in: [Cliff_walking](Cliff_walking)

## Overview of the methods
Policy: $$ \pi(s,a) = Pr(a=a|s=s)$$
Value function: $$ V_{\pi}(s)=\mathbb{E}[\sum_{t=1}^\infty\gamma^tr(s_{t})]$$

The objective is to find the optimal pollicy to maximize future rewards. 

### Model based RL with Markov Decision Process
We have a deterministic propability $P(s',s,a)$ function which defines the probability of moving from state $s$ to state $s'$ given action $a$.
The model basded algortithme is based on Bellman's function and Dynamic programming. 
#### Value iteration
* Initialize Value function with zero to every possible states
* Iterate over each state until it converge to such tolerance
* Output a deterministic policy which maximzes the value function

### Policy iteration
* Randomly initialize the policy 
* Two step plicy 
    * Iteratively update the value function by locking in that policy
    * Iteratively update the policy function by locking the value function until convergence

### Model free RL with Q-learning
Introduce of a $Q$ function, which is a joint possibility of state/action pair. 
While the 
$$Q(s,a)= \mathbb{E}(R(s',s,a)+\gammav(s'))$$

which one converge fast 





 




