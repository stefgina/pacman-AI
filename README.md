# Pacman AI
```python

Author -> Stefanos Ginargyros

```


## 1. Depedencies

In order to execute the game properly (+ the AI functionality), you will have to:

```
pip install pygame
pip install py_trees
``` 

Decision Trees further boost the pacman agent with AI capabillities. For more information about the library read [here](https://py-trees.readthedocs.io/en/devel/).


## 2. Description
  
AI pacman implementation in pure Python. It depends only in basic python libraries such as numpy and pygame. The A pacman agent runs with two independent but equal functionality modules. A Behaviour tree and a Finite State Machine. Both of these modules end up utilizing the same set of actions (such as Eat Pills, Escape the Ghosts, Ignore the ghosts). The escence of these actions lies in minimization/ maximization of Euclidean distances between pacman and a target (ghosts or pills). The pygame gameflow consists of a launch-screen, and a main game loop where the program can also wait for button presses for a human player to control pacman if needed. There is also score-keeping functionality. Here is a preview of the main game-state:


<img src="https://github.com/stefgina/pacman-python-AI/blob/main/pacman2.png" width="345" height="415"/>


## 3. Behaviour Tree

The behaviour tree was implemented inside the framework py-trees. It is an open source library for fast behaviour-tree implementations in C++ wrapped up in Python. The root node is a Selector node which selects between 3 actions. Every action is implemented as a different class, which inherrits from pytrees.Behaviour libray. The tree works with a single tick(), on every single frame of the game loop. The tick (pulse) starts from root node, checks the conditions for every action and return SUCESS or FAILURE accordingly. If the output of the action is SUCCESS then the tree stops ticking for the particular frame. If it is FAILURE the tick() goes to the lower priority action-nodes and checks for conditions.

<img src="https://github.com/stefgina/pacman-python-AI/blob/main/tree.png" width="355" height="465"/>

## 3. Finite State Machine

The finite state machine was implemented in the context of if-else statements in python, due to the lack of switch-case. It utilizes the same functionality and actions as the behaviour tree. The states are Escape Ghosts, Eat Pills, Ignore Ghosts. The condition in most cases is the euclidean distance from Pacman to the ghosts. It is considered as safe if its above a certain threshold and in that case we are in the state of Eat Pills. If its bellow the threshold then he have to escape the ghosts, by maximizing the euclidean distance to the ghosts. Another condition is if ghosts are distressed where pacman even if hes in the danger zone he can continue his pill-munching journey.

<img src="https://github.com/stefgina/pacman-python-AI/blob/main/fsm.png" width="355" height="465"/>





