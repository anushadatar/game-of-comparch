---
layout: "default"
title: Overview
---
# Game of CompArch: Cellular Automata and Computing
An exploration of the use of cellular automata to perform complex computations, culminating in the implementation of an
Arithmetic Logic Unit (ALU) in John Conway's Game of Life.

- - - -
## Introduction to Cellular Automata
Cellular automata are spatially- and temporally-discrete systems that develop through a serious of time steps according to a set of rules.
These rules are constrained in that a cell can only be affected by a neighboring cell (no action at a distance) and all the
rules must be abstract and able to be described purely mathematically. Because of this, cellular automata are typically computational
systems that can sometimes be shown to be Turing complete.

One of the simplest examples of cellular automata is a one-dimensional system with each cell assuming a state of either "on" (black)
or "off" (white). Let's say it follows a set of rules like the ones shown below, where the second-row cell shows the evolution resulting
from the top-row condition when following these rules.

![OneDimensionalRules](http://mathworld.wolfram.com/images/eps-gif/ElementaryCA30Rules_750.gif)

The image below shows this configuration iterating through many time steps. You can see that, even a one-dimensional system
with an initial condition of one "on" block results in intricate patterns over time! This particular pattern is used in Mathematica
as a large-integer random-number generator due to the aperiodic, chaotic behavior that it exhibits.

![OneDimensionalExample](http://mathworld.wolfram.com/images/eps-gif/ElementaryCA30_1000.gif)

Cellular automata were conceived by John von Neumann in the 1950s and originally used by him to create self-replicating
systems. The system created by him was fairly complicated, with each cell able to be in one of 29 different states. Historically,
cellular automata have been useful platforms for modelling dynamic systems and for conceptually studying pattern formation. More
recently they've also become topics of philosophical discussion, as the complex emergent patterns in cellular automata raise questions about
emergent theories of the origins of life and a computational universe's relationship with determinism.


- - - -
## The Game of Life
![GameofLifeForFun](https://media.giphy.com/media/tXlpbXfu7e2Pu/giphy.gif)

Proposed by John Conway in 1970, the *Game of Life* is now one of the most well-known
cellular automata systems ever created.

The Game of Life is a 2-dimensional binary system with a Moore neighborhood. At each time step, the cells can take one of three actions:
> 1. Survival: If the cell was on and either two or three neighbors were on, the cell remains on
> 2. Birth: If the cell was off and exactly three of its neighbors were on, the cell turns on
> 3. Death: If the cell was on and fewer than two or more than three neighbors were on, the cell turns off

These simple rules give rise to many observable complex behaviors. A small community built itself around Conway's Game of Life, exploring the useful
stable configurations that arise from certain starting conditions. Commonly used objects include *blinkers* that repeat their states after a certain
number of time steps, *gliders* that travel across the grid, or *guns* that generate a stream of gliders. Configurations can become incredibly complex,
with large starting configurations resulting in stunning evolutions that almost seem to be alive.

![GameofLifeForFun](https://media.giphy.com/media/uet5GfHpSA8mI/giphy.gif)

Philosopher Ilachinski, well known for his work in the field of cellular automata, says about this features of the Game of Life
 > Upon observing the seemingly unlimited complexity and variety of *Life's* evolving patterns, it becomes almost impossible to refrain from imagining,
 > along with Conway, that, were the game really to be played on an infinite lattice, there must surely arise true living "life forms", perhaps themselves
 > evolving into more complex, possibly sentient, "organisms".(Ilachinski 2001: 133)

Using these configurations that have been invented (or found) by users of the Game of Life, we can create basic computational elements. With streams of gliders
representing logical 1's and 0's, all the basic logic gates can be made, such as the *AND* gate shown below. By showing that these building blocks of computation
can be made robustly and consistently, it seems as if any computation that can be performed by a traditional computer could theoretically be implemented in the
Game of Life. In fact, *Life* has been proven to be Turing-complete --

- - - -
