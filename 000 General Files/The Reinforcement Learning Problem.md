## 3.1 The Agent-Environment Interface
**Agent**: Learner and decision maker
**Environment**: The thing it interacts with, basically everything other than the agent

These interact continually, with the agent selecting actions and the environment responding to those actions and presenting new situations to the agent. The environment also gives rewards that the agent tries to maximize over time. 
![[Pasted image 20250204102946.png]]
![[Pasted image 20250204103134.png]]
**Policy**:  $\pi_t(s,a)$ At each time step, the agent maps states to probabilities of selecting each possible action.

Reinforcement learning methods specify how the agent changes its policy as a result of its experience. The goal is to maximize its rewards. Ultimately, this framework can be as high or low level as necessary in terms of its representation of a reinforcement learning method.

**Agent Environment Boundary**: represents the limit of the agent's *absolute control*, not of its knowledge.

**States** and **Actions** are usually represented as vectors or matrices. **Rewards** are just single numbers.
## 3.2 Goals and Rewards
In RL, the reward is a signal passing from the environment to the agent. The reward can change at each time step, but it is always a number. The agent wants to maximize the cumulative reward, not immediate.

In this way, agents always want to maximize rewards. We must construct the reward system to encourage it to complete a goal. Specifically to complete the goal, not how to complete it.
## 3.3 Returns
## 3.4 Unified Notation for Episodic and Continuing Tasks
## 3.5 The Markov Property
## 3.6 Markov Decision Processes
## 3.7 Value Functions
## 3.8 Optimal Value Functions
## 3.9 Optimality and Approximation
## 3.10 Summary
