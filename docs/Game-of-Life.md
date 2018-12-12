---
layout: "default"
title: Conway's Game of Life
---

# Conway's Game of Life
## Overview
Conway's Game of Life is a well-known simple cellular automaton. Its behavior is quite straightforward: 
* The *lattice* is an infinite grid of black and white cells.
* The *state* of each cell is whether the color of the cell is black or white.
* The *neighborhood* of the cell is the eight cells around it.
* The transition *function* is based on a few constraints:
** Survival: If the cell was on and either two or three neighbors were on, the cell is balck,
** Birth: If the cell was off and exactly three of its neighbors were on, the cell turns on
** 3. Death: If the cell was on and fewer than two or more than three neighbors were on, the cell turns off

## Patterns and Properties
From these rules come a large number of patterns common to the game. These patterns include
* 
* 
* *Gliders* : 
* *Glider Guns* :

Many researchers believe that one of the special properties of the Game of Life -- the one that allows these configurations to happen, and the reason why the Game has been so philosophically and computationally interesting -- is that it lies near the *edge of chaos*. Or, the patterns it produces don't usually tend towards a completely stable state, nor do their results appear to be completely random. The near-ness to the edge of chaos is quantified by a parameter called \lambda, which is the fraction of a cellular automata's rules that lead to the "life" of a cell.