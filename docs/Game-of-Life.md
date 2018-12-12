---
layout: "default"
title: Conway's Game of Life
---

# Conway's Game of Life
## Overview
Conway's Game of Life is a well-known simple cellular automaton. Its behavior is quite straightforward:
* The *lattice* is an infinite grid of black and white cells.
* The *state* of each cell is whether the color of the cell is black or white (also commonly referred to as "dead" or "alive", respectively).
* The *neighborhood* of the cell is the eight cells around it.
* The transition *function* is based on a few constraints:
>Survival: If the cell is alive and two or three of its neighbors are alive, the cell remains alive

>>Birth: If the cell is dead and exactly three of its neighbors are alive, the cell becomes alive

>>Death: If the cell is alive and fewer than two or more than three of its neighbors are alive, the cell dies

## Patterns and Properties
From these rules come a large number of patterns common to the game. These patterns include
* *Oscillators* : a group of cells that periodically repeat patterns in place
![Oscillator](https://i0.wp.com/mathblog.com/wp-content/uploads/2011/05/game_toad.gif?ssl=1)

* *Gliders* : small clusters of cells that travel across the lattice
![Glider](https://i0.wp.com/mathblog.com/wp-content/uploads/2011/05/game_glider_fast.gif?ssl=1)

* *Glider Guns* : structures that produce a steady stream of gliders
![Gun](https://upload.wikimedia.org/wikipedia/commons/e/e5/Gospers_glider_gun.gif)

Small structures can be combined to form larger and more computationally interesting structures. The most obvious example of this is the creation of
logic gates. Below we can see examples of an AND, OR, and NOT gate, respectively.

![AND](https://camo.githubusercontent.com/5190f70598d5e917797dc64ab5713165946cb3de/68747470733a2f2f6d656469612e67697068792e636f6d2f6d656469612f336f39624f5464505377337147315a396f642f67697068792e676966)

![OR](https://camo.githubusercontent.com/110216dd8ac588867bd1d7f687f932d740d5d673/68747470733a2f2f6d656469612e67697068792e636f6d2f6d656469612f3535764565714c52626f31734e7330456b462f67697068792e676966)

![NOT](https://camo.githubusercontent.com/6729e9a4329c342be81355dc4b3fa430623c7b4d/68747470733a2f2f6d656469612e67697068792e636f6d2f6d656469612f524d6466756d324a4954556e3941717543702f67697068792e676966)


This is incredibly significant -- knowing that we can create any logic function using
the *Game of Life* leads us to the conclusion that we could create full computers using only the *Game of Life* as a platform.
In fact, this has been proven. Conway and a few others proved shortly after the creation of the *Game of Life* that it is Turing-complete
and can theoretically be used to compute anything that is computable. The first *Game of Life* Turing machine was created by Paul Rendell and can
duplicate a pattern of ones that it is fed.

![TuringMachine](https://archive.li/obdP1/163c8047c09eb685e9eea1c5db9e76ca7731dffa.gif)

Further work has even shown that full CPUs can be constructed entirely using the *Game of Life*.

Many researchers believe that one of the special properties of the Game of Life -- the one that allows these configurations to happen, and the reason why the Game has been so philosophically and computationally interesting -- is that it lies near the *edge of chaos*. Or, the patterns it produces don't usually tend towards a completely stable state, nor do their results appear to be completely random. The near-ness to the edge of chaos is quantified by a parameter called \lambda, which is the fraction of a cellular automata's rules that lead to the "life" of a cell -- the edge is defined to be at or around a \lambda value of 0.5. Many of the cellular automata that have been shown to be Turing-complete, including the *Game of life*, have \lambda values that are close to the edge value.
