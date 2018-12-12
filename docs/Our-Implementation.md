---
layout: "default"
title: Our Implementation
---
# Our Implementation
 
 In order to create the structures of a compute in the game of life, we have to implement physical structures to produce, relay, and modify information. Due to the underlying logic gate structure of computers, we could build almost any structure using a combination of logic gates, traces to connect gates, and voltage sources to drive the inputs for the logic gates.
 
 ## Voltage Sources and Wiring
 In real-life systems, information is transmitted across computers through digital signals: a combination of high and low voltages pread over time. This digital stream of 1s and 0s is emulated in the game of life by the presence or absence of glider in a glider stream.
 
 The following image depicts a glider stream that is transmitting a stream of 1s.
 ![stream of gliders](images/wire_1_small.PNG)
 
 A lack of gliders would indicate a transmission of all 0s.
 ![stream of 0s](images/wire_0_small.PNG)

Due to the large propogation delay of logic gates relative to the amount of gliders that pass through them, each digital signal would have to contain on the order of 50 or more gliders to prevent any hazards.

In order to continually generate signals to pass through our hardware, we used the Gosper Glider Gun in combination with an eater block to control whether or not we were producing a glider stream. 
![gosper gun](https://en.wikipedia.org/wiki/File:Gosper_glider_gun_with_grid.gif)

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
