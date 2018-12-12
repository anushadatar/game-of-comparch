---
layout: "default"
title: Mathematically Describing Cellular Automata
---

# Describing Cellular Automata

One of the hallmarks of cellular automata is that they can be described abstractly. The rules that a system follows can be defined with relatively straightforward state-based models and functions.

The state of a cellular automaton at some point can be defined by: 
* **Z** : The *lattice*, or the grid the game is conducted upon. In the case of the game of life, this would refer to t
* **S** : The set of *state variables* for each cell.
* **N** : The finite *neighborhood*, or cells related to some observed cell.
* **F** : The transition *function* associated with the given rule.
The tuple *(Z, S, N, F)* defines the state and behavior of a given automaton based on these parameters. At each timestep increment, the states of the cells change based on the transition function.

### Definitions

### Neighborhoods and Stability
TODO Wolfram's classifications and types of machines,


### Rules and Functions
In general, the local transition function maps an lattice of cells with certain states at some timestep to a new set of cells with certain states based on the function specified by the rule and the existing states of the cells in the neighborhood of the cell under study. These functions generally take the form of a conditional expression:

## Turing Machines


## Emergent Behavior
### Reversibility 

### Halting
Cell
At its core, the halting problem is the quesiton of whether a machine, when given an arbitrary program and input, can determine whether or not this program will finish running or run continuously.

### The Edge of Chaos