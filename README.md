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


## 1. Description
  
AI pacman implementation in pure Python. It depends only in basic python libraries such as numpy and pygame. The A pacman agent runs with two independent but equal functionality modules. A Behaviour tree and a Finite State Machine. Both of these modules end up utilizing the same set of actions (such as Eat Pills, Escape the Ghosts, Ignore the ghosts). The escence of these actions lies in minimization/ maximization of Euclidean distances between pacman and a target (ghosts or pills). The pygame gameflow consists of a launch-screen, and a main game loop where the program can also wait for button presses for a human player to control pacman if needed. There is also score-keeping functionality. Here is a preview of the main game-states:

<p float="left">
<img src="https://github.com/stefgina/pacman-python-AI/blob/main/pacman1.png" width="375" height="465"/>
<img src="https://github.com/stefgina/pacman-python-AI/blob/main/pacman2.png" width="375" height="465"/>
</p>

