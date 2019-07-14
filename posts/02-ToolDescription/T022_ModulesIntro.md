---
layout: default
title: Navindoor modules
nav_order: 2
has_children: true
parent: Navindoor description

---

Navindoor has been developed under the paradigm of object-oriented programming. Classes have been defined to represent elements in the design of location systems. The planimetry, trajectories or signals are classes that contain associated methods for their visualization, data extraction and interaction between them. On the other hand, we have location algorithms and metrics to compare algorithms. These are represented by functions that act on the above mentioned classes.
These classes and functions have been developed in five modules that follow the process of experimentation in the design of location systems. In order to have a global vision of it, this process and the module proposed in each point will be briefly described:
1. Obtaining the planimetry. The first step in the experimentation is the choice of the scenario and the obtaining of the planimetry. In Navindoor, the planimetry module has been created with the necessary classes for
to build a multi-level planimetry.
2. Generation of trajectories. In the experimentation, reference points are taken in order to be able to construct trajectories through them. This limits the variety of trajectories, however it is necessary to obtain
precise measurements of the position at any given moment. Navindoor has created the module for generating trajectories, dedicated to the simulation of trajectories. Because we are in a simulation environment we have exact information about the real trajectory, generated from a succession of points provided by the user.
3. Signal measurement. In experimentation, once the trajectory has been generated, it must be enriched with signals. The third module, called the signal generation module, is dedicated to simulation.
of synthetic signals. Thanks to simulation, we can create the signals after the trajectory has been generated.
4. Signal processing. After taking measurements, the locating algorithms process the signals. The fourth Navindoor module, called the measurement processing module, provides algorithms capable of creating estimates of the real trajectory from the simulated signals. It also offers a scheme where new algorithms can be developed.
5. Algorithm Comparison. Finally, in order to validate the developed algorithms it is necessary to compare them with other already consolidated algorithms. The fifth module of Navindoor is the validation module of 
algorithms, which provide us with methods of comparing algorithms provided by the user or between algorithms by default.

Within these modules are distributed the classes and functions defined in Navindoor. 
It is worth mentioning that both CLI and GUI are compatible in MATLAB versions higher than MATLAB R2017b. 
Details of each module are presented next. 