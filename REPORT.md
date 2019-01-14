### Introduction

In this project I solved a double-jointed arm environment where the goal of the agent was to maintain its position at the target location for as many time steps as possible.

The task was episodic and in order to solve the environment, the agent must get an average score of +30 over 100 consecutive episodes.

### Learning Algorithm

The algorithm I used to solve the environment is Deep Deterministic Policy Gradient.

I tried different network architectures for the model. I introduced more layers to actor and critic algorithms with different nodes, but none of these helped improve training, resulting 1000 episodes with Average Score less than 1.

Then I tried batch normalization with a simple two fully connected layer architecture with 128 nodes each layer. This improved training dramatically.

Hyperparameters I used are:

```
BUFFER_SIZE = int(1e5)  # replay buffer size
BATCH_SIZE = 128        # minibatch size
GAMMA = 0.99            # discount factor
TAU = 1e-3              # for soft update of target parameters
LR_ACTOR = 2e-4         # learning rate of the actor 
LR_CRITIC = 2e-4        # learning rate of the critic
WEIGHT_DECAY = 0        # L2 weight decay
```


### Plot of Rewards:
Below is the plot and the final training average scores over 100 episodes.
![Alt text](/continuous_control_plot.png?raw=true "Final Training Results")


### Ideas For Future Work:
I would like to try different alsorithms like PPO, A3C for both the first and the second version of the environment. I would be interested to see how these algorithms would perform with respect to each other in both these environments.