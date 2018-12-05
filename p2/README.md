[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/43851024-320ba930-9aff-11e8-8493-ee547c6af349.gif "Trained Agent"


# Project 2: Continuous Control

This folder contains a solution to Project 2 in "Deep Reinforcement Learning" at Udacity.

### Introduction

The goal is to solve the [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) environment.

![Trained Agent][image1]

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the agent's goal is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

### Distributed Training

There are two separate versions of the Unity environment:
- The first version contains a single agent.
- The second version contains 20 identical agents, each with its own copy of the environment.  

Here, the second version is used. The environment is considered solved when the average (over 100 episodes) of those average scores is at least +30. That is, the agents must get an average score of +30 (over 100 consecutive episodes, and over all agents). Specifically,
- After each episode, rewards that each agent received (without discounting) are added up to get a score for each agent.  This yields 20 (potentially different) scores. These 20 scores are then averaged.  
- This yields an **average score** for each episode (where the average is over all 20 agents).


### Getting Started

1. Download the environment from one of the links below. Select the environment that matches your operating system:

    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)    

2. Unzip the file (e.g. in the current folder) and update the `Continuous_Control.ipynb` notebook to point to the location. 

3. Follow the recipe found [here](https://github.com/udacity/deep-reinforcement-learning#dependencies) to install and configure necessary dependencies.

### Instructions

To train an agent or watch pre-trained agents, follow the instructions in `Continuous_Control.ipynb`. In addition to the notebook, the code for the agent can be found in `ddpg_multiagent.py` and the neural net used by the agent is defined in `model.py`.
