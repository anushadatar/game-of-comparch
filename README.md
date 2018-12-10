# Game of CompArch: Cellular Automata and Computing
An exploration of the use of cellular automata to perform complex computations, culminating in the implementation of an
Arithmetic Logic Unit (ALU) in John Conway's Game of Life.

- - - -
## Introduction to Cellular Automata
Cellular automata are spatially- and temporally-discrete systems that develop through a serious of time steps according to a set of rules.
These rules are constrained in that a cell can only be affected by a neighboring cell (no action at a distance) and all the
rules must be abstract and able to be described purely mathematically. Because of this, cellular automata are typically computational
systems that can sometimes be shown to be Turing-complete.

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
cellular automata have been useful platforms for modelling dynamic systems and for conceptually studying pattern formation. Because cells in
a cellular automata are only affected by their immediate neighbors, they're useful for modelling physical systems that are only directly affected
by the space immediately adjacent to them. This tendency to only interact with neighbors also means that cellular automata can accurately model
delays, like wave propagation. So, the most widespread practical use of cellular automata is modelling physical interactions over long periods of
time that evolve according to pre-set rules. Some of the fields this has been applied in extensively include traffic modelling, studying patterns in
genetics, and visualizing fluid flows.

(I'd like to include a figure or something here that shows an implementation of something useful with a CA)


More recently, cellular automata have also become a topic of philosophical discussion, as the complex emergent patterns in cellular automata raise questions about
emergent theories of the origins of life and a computational universe's relationship with determinism.


- - - -
## Mathematically Describing Cellular Automata

One of the hallmarks of cellular automata is that they can be described abstractly. The rules that a system follows can be defined with
functions.

However, despite this low-level mathematical description of these systems, our predictions of their behavior break down over large spatial and
time scales.

Many researchers believe that one of the crucial properties of computationally-significant cellular automata --
the one that allows standard, complex configurations to happen, and the reason why some automata have been
so philosophically and computationally interesting -- is that they lies near the *edge of chaos*. Or, the patterns they produce don't usually tend towards a completely stable state,
nor do their results appear to be completely random. The near-ness to the edge of chaos is quantified by a parameter called \lambda, which is the fraction of a cellular automata's
rules that lead to the "life" of a cell.


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

Using these configurations that have been discovered by users of the Game of Life, we can create basic computational elements. With streams of gliders
representing logical 1's and 0's, all the basic logic gates can be made, such as the *AND* gate shown below. By showing that these building blocks of computation
can be made robustly and consistently, it seems as if any computation that can be performed by a traditional computer could theoretically be implemented in the
Game of Life. In fact, *Life* has been proven to be Turing-complete --

- - - -
## Our Project
Our final goal was to implement an Arithmetic Logic Unit (ALU) in the Game of Life that could perform several different operations on two 4-bit numbers. The first
step in this process is the design of the ALU itself. A block diagram of what we aimed to build can be seen below.

(block diagram of ALU)

An implementation in the Game of Life necessitates that our design be at the gate level so we can translate it into Conway's system using logic gate building blocks
that already exist. We've tried to use the simplest possible designs to facilitate building in the Game of Life.

(details about y the alu is the way it is)

To run our ALU we're using Golly, an open-source cellular automata simulator with lots of support for modularity of designs and scripts that make undertakings
of this complexity a bit more straightforward. We've been in contact with a student called Nicolas who built an entire CPU using the Game of Life as a platform --
he's shared his git repository with us, which is what we've been using as a source for the logic gates and basic blocks like *eaters* and *delays* in our design.


- - - -
## Results and Discussion

What does our ALU look like? Did we succeed?

- - - -
## Conclusion

Which problems are best suited to being solved with CA, and what emerging technologies are there that CA is a large part of?
While this exercise isn't really significant in any engineering capacity, what cool things have we shown about CA?

- - - -
## Sources
https://plato.stanford.edu/entries/cellular-automata/#CAPhilComp
https://www.wolframscience.com/nks/notes-2-1--cellular-automaton-rules-as-formulas/
http://eprints.uwe.ac.uk/22323/1/thesis.pdf
https://annarchive.com/files/Winning%20Ways%20for%20Your%20Mathematical%20Plays%20V1.pdf
