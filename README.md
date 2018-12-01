# Game of CompArch: Cellular Automata and Computing
An exploration of the use of cellular automata to perform complex computations, culminating in the implementation of an
Arithmetic Logic Unit (ALU) in John Conway's Game of Life.

## What are Cellular Automata?
Cellular automata are spatially- and temporally-discrete systems that develop through a serious of time steps according to a set of rules.
These rules are constrained in that a cell can only be affected by a neighboring cell (no action at a distance) and all the
rules must be abstract and able to be described purely mathematically. Because of this, cellular automata are typically computational
systems that can be shown to be Turing-complete.

One of the simplest examples of cellular automata is a one-dimensional system with each cell assuming a state of either "on" (black)
or "off" (white). Let's say it follows a set of rules like the ones shown below, where the second-row cell shows the evolution resulting
from the top-row condition when following these rules.

![OneDimensionalRules](http://mathworld.wolfram.com/images/eps-gif/ElementaryCA30Rules_750.gif)

The image below shows this configuration iterating through many time steps. You can see that, even a one-dimensional system
with an initial condition of one "on" block results in complex patterns over time! This particular pattern is used in the Wolfram
programming language as a random-number generator.

![OneDimensionalRules](http://mathworld.wolfram.com/images/eps-gif/ElementaryCA30_1000.gif)

Cellular automata were conceived by John von Neumann in the 1950s and originally used by him to create self-replicating
systems. The system created by him was fairly complicated, with each cell able to be in one of 29 different states. A much simpler
cellular automata system was proposed by John Conway in 1970 known as his Game of Life, which is now one of the most well-known
cellular automata systems ever created. The Game of Life was proven to be Turing-complete in 1982 and is the platform that we
used to construct our ALU.
