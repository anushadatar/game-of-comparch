# Game of CompArch: Cellular Automata and Computing
An exploration of the use of cellular automata to perform complex computations, culminating in the implementation of an
Arithmetic Logic Unit (ALU) in John Conway's Game of Life.

- - - -
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
programming language as a large-integer random-number generator due to the chaotic patterns that it produces.

![OneDimensionalExample](http://mathworld.wolfram.com/images/eps-gif/ElementaryCA30_1000.gif)

- - - -
## What is the Game of Life?
![GameofLifeForFun](https://media.giphy.com/media/tXlpbXfu7e2Pu/giphy.gif)

Cellular automata were conceived by John von Neumann in the 1950s and originally used by him to create self-replicating
systems. The system created by him was fairly complicated, with each cell able to be in one of 29 different states. A much simpler
cellular automata system was proposed by John Conway in 1970, known as his Game of Life, which is now one of the most well-known
cellular automata systems ever created.

The Game of Life is a 2-dimensional binary system with a Moore neighborhood. At each time step, the cells can take one of three actions:
> 1. Survival: If the cell was on and either two or three neighbors were on, the cell remains on
> 2. Birth: If the cell was off and exactly three of its neighbors were on, the cell turns on
> 3. Death: If the cell was on and fewer than two or more than three neighbors were on, the cell turns off

These simple rules give rise to many observable complex behaviors. A small community built itself around Conway's Game of Life, exploring the useful
stable configurations that arise from certain starting conditions. Commonly used objects include *blinkers* that repeat their states after a certain
number of time steps, *gliders* that travel across the grid, or *guns* that generate a stream of gliders.

![Blinker](https://i0.wp.com/mathblog.com/wp-content/uploads/2011/05/game_toad.gif?ssl=1) ![Glider](https://i0.wp.com/mathblog.com/wp-content/uploads/2011/05/game_glider_fast.gif?ssl=1) ![Gun](https://aidanfray.files.wordpress.com/2016/03/gosperglidergun.gif?w=470)

One of the main special properties of the Game of Life -- and the reason why it has been
so computationally and philosophically interesting -- is
