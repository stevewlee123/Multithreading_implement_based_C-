# Multithreading_implement_based_Cpp

This is a simulation of the daily work of a plant.

## Problem Description

Condider a plant, where there are several part workers and product workers whose jobs are to produce one type of item. This item needs five types of parts to assemble.

There is a buffer state (a place where the part workers will load all the parts to and the product works will obtain parts from).

There are total five types of parts.

### Part Workers

Each part worker will produce 5 pieces of all possible combinations, such as (2,0,0,2,1), (0,2,0,0,3), (5,0,0,0,0), etc., given that it takes 50, 50, 60, 60, 70 microseconds to make each part of type A, B, C, D, E, respectively. Each part worker will attempt to load the produced parts to a buffer area, and it will take a part worker 20, 20, 30, 30,40, us to move a part of type A, B, C, D, E, respectively, to the buffer.

### Product Workers

Each part worker will obtain parts from the buffer state and assemble the product. Each product assembly needs five pieces of parts each time. However, the five pieces will be from exactly two or three types of parts, such as (1,2,2,0,0), (1,0,3,1,0), (1,0,0,0,4), (0,2,3,0,0), etc. with equal occurrence probability, and it will take a part worker 20, 20, 30, 30,40, us to move a part of type A, B, C, D, E, respectively, from the buffer.

### Buffer State

The buffer state has a capacity of (5,5,4,3,3). If any type of part is full, the part worker or product worker need to wait for the availability. Also, each part woker and product work has a waiting time and if the buffer state is still not avaiable after the waiting time, the part worker or product worker should bring back whatever they have at that moment and come back in next round.