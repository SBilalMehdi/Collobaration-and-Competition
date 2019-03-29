[//]: # (Image References)
[image]: https://github.com/Unity-Technologies/ml-agents/blob/master/docs/images/tennis.png "Tennis"

# Project 3: Collaboration and Competition

## Introduction

This repository serves as a submission for "Collaboration and Competition" Project for the Deep Reinforcement Learning Nanodegree offered by Udacity. The code contained in this repository is a modified version of sample codes provided in different exercises in the Nanodegree. 

## Environment 

The repository is used with a modified version of [Tennis](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#tennis) Environment as provided in the Udacity Nanodegree.

![Tennis][image]

In this environment, two agents control rackets to bounce a ball over a net. If an agent hits the ball over the net, it receives a reward of +0.1. If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01. Thus, the goal of each agent is to keep the ball in play.

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation. Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.

The task is episodic, and in order to solve the environment, your agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,

Markup : * After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores.
         * This yields a single score for each episode.

### Solving the Environment

The environment is considered to be solved if the agent gets an average score of +30 (over 100 consecutive episodes, and over all agents).  Specifically,
- After each episode, add up the rewards that each agent received (without discounting), to get a score for each agent.  This will yield 20 (potentially different) scores.  Then take the average of these 20 scores. 
- This will yield an **average score** for each episode (where the average is over all 20 agents).

The environment is considered solved, when the average (over 100 episodes) of those average scores is at least +30. 

## Python Packages Required

- numpy
- collections
- torch
- pickle
- matplotlib
- random

## Getting Started

For this project, you will not need to install Unity - this is because we have already built the environment for you, and you can download it from one of the links below. You need only select the environment that matches your operating system:

* Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
* Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
* Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
* Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)

Then, place the file in the p3_collab-compet/ folder in the DRLND GitHub repository, and unzip (or decompress) the file.

(For Windows users) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

(For AWS) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux_NoVis.zip) to obtain the "headless" version of the environment. You will not be able to watch the agent without enabling a virtual screen, but you will be able to train the agent. (To watch the agent, you should follow the instructions to enable a virtual screen, and then download the environment for the Linux operating system above.)(For Windows users) Check out this link if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

(For AWS) If you'd like to train the agent on AWS (and have not enabled a virtual screen), then please use this link to obtain the "headless" version of the environment. You will not be able to watch the agent without enabling a virtual screen, but you will be able to train the agent. (To watch the agent, you should follow the instructions to [enable a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md), and then download the environment for the Linux operating system above.)

## Description of Each File

| File Name             | Description                                                                    |
|-----------------------|--------------------------------------------------------------------------------|
| agent.pt    | Trained DDPG agent|
| Tennis.ipynb    | Main file that trains a DDPG agent|
| Readme.md    | This readme |
| Report.pdf    | A short report on the project |
| ddpg_agent.py    | Python code that contains the algorithmic implementation of DDPG |
| model.py    | A python file that defines the neural network objects used by the DDPG agent |
