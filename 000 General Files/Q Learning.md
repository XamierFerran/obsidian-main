Source: https://www.geeksforgeeks.org/q-learning-in-python/#qlearning-in-reinforcement-learning

## Key Components of Q-Learning
### 1. Q-Values or Action Values
Q values are defined for states and actions. $Q(S,A)$ is an estimation of how good it is to take the action A at the state S. The estimation of $Q(S,A)$ will be iteratively computed.
### 2. Rewards and Episodes
Agent starts from a start state. The agent moves from the start state to the next state based on its choice of action and also the environment the agent is interacting in. After every action the agent observes a reward from the environment. The agent arriving at a terminating state is the completion of the episode.
### 3. Temporal Difference or TD-Update
This update rule is used to estimate the value of Q at every time step.$$Q(S,A)\leftarrow Q(S,A) + \alpha(R+\gamma Q(S',A')-Q(S,A))$$
- S: Current State of the agent.
- A: Current Action Picked according to some policy.
- S’: Next State where the agent ends up.
- A’: Next best action to be picked using current Q-value estimation, i.e. pick the action with the maximum Q-value in the next state.
- R: Current Reward observed from the environment in Response of current action.
- γγ(>0 and <=1) : Discounting Factor for Future Rewards. Future rewards are less valuable than current rewards so they must be discounted. Since Q-value is an estimation of expected rewards from a state, discounting rule applies here as well.
- αα: Step length taken to update the estimation of Q(S, A).
### 4. Selecting a course of action with $\epsilon$-greedy policy
**$\epsilon$-greedy policy**: A simple method of selecting an action to take based on the current estimates of the Q-value. This is how it operates
#### Superior Q-Value Action (Exploitation):
#### Exploration through random action
