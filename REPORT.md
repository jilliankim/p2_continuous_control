### Introduction

In this project I solved a double-jointed arm environment where the goal of the agent was to maintain its position at the target location for as many time steps as possible.

The task was episodic and in order to solve the environment, the agent must get an average score of +30 over 100 consecutive episodes.

### Learning Algorithm

The algorithm I used to solve the environment is Deep Deterministic Policy Gradient.

I tried different network architectures for the model. I introduced more layers to actor and critic algorithms with different nodes, but none of these helped improve training, resulting 1000 episodes with Average Score less than 1.

### Plot of Rewards:
Below is the plot and the final training average scores over 100 episodes.
![Alt text](/continuous_control_plot.png?raw=true "Final Training Results")

