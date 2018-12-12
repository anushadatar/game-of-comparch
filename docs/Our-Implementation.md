---
layout: "default"
title: Our Implementation
---
# Our Implementation

## ALU Design
The construction of our computational element, an Arithmetic Logic Unit, started with the creation of a block diagram. While we initially wanted our ALU to be able to perform all of the operations required by the MIPS architecture, we quickly pared this down to fit within the time constraints of the project. We settled on a 4-operation, 4-bit ALU that can add, subtract, XOR, and AND two binary numbers.

(put block diagram here)

In the *Game of Life* everything is constructed at gate-level, so we also needed to dive deeper into each block and produce a schematic comprised of logic gates. The breakdown for one bit can be seen below.

(Logic gate schematic)

 In order to create the structures of a computer in the game of life, we have to implement physical structures to produce, relay, and modify information. Due to the underlying logic gate structure of computers, we could build almost any structure using a combination of logic gates, traces to connect gates, and "voltage sources" to drive the inputs for the logic gates.
 
## Analogues of Voltage Sources and Wiring
 In real-life systems, information is transmitted across computers through digital signals: a combination of high and low voltages read over time. This digital stream of 1s and 0s is emulated in the *Game of Life* by the presence or absence of gliders in a glider stream.

 The following image depicts a glider stream that is transmitting a stream of 1s.

 ![stream of gliders](images/wire_1_small.png)

 A lack of gliders would indicate a transmission of all 0s.

 ![stream of 0s](images/wire_0_small.png)

Due to the large propagation delay of logic gates relative to the amount of gliders that pass through them, each digital signal would have to contain on the order of 50 or more gliders to prevent any hazards.

In order to continually generate signals to pass through our hardware, we used the Gosper Glider Gun in combination with an eater block to control whether or not we were producing a glider stream.
![gosper gun](https://upload.wikimedia.org/wikipedia/en/5/5d/Gosper_glider_gun_with_grid.gif)

## Logic Gates
The following logic gate structures were obtained from [nicolasloizeau](https://github.com/nicolasloizeau/gol-computer).

#### AND
![and](https://media.giphy.com/media/3o9bOTdPSw3qG1Z9od/giphy.gif)

#### XOR
![xor](https://media.giphy.com/media/iMCj4EgPkQOvetoPuV/giphy.gif)

#### NOR
![nor](https://media.giphy.com/media/182tC6OM2QTsCUuKrl/giphy.gif)

#### OR
![or](https://media.giphy.com/media/55vEeqLRbo1sNs0EkF/giphy.gif)

#### NOT
![not](https://media.giphy.com/media/RMdfum2JITUn9AquCp/giphy.gif)

## Hazards
As a glider moves through the lattice, it oscillates between 4 phases. Structures that interact with gliders are very picky and will only couple properly if the glider stream comes into contact with structure at the right phase. Unfortunately, most actions that affect a stream will set the stream out of phase. To compensate for shifting phases, strategic delay blocks need to be added to keep traces in phase.

If any traces need to overlap, they must be shifted out of phase or else the gliders will destructively interfere and propagate false 0s.

## Construction and Final Result
To run the *Game of Life* we used the open-source application Golly. The scripts included with Golly that placed the cells were written with quad trees that were incomprehensible to us, so we placed and routed our ALU by hand (this process certainly built character).

By first building each individual component (add/sub module, mux, individual logic gates) we were able to use a bitwise architecture to simplify the building of our final product.

Our final ALU can be seen below, adding the numbers (A) and (B)!

(ALU here pls)

## Reflection
