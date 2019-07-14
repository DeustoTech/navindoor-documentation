---
layout: default
title: State of the Art of Simulators for Localization
nav_order: 1
has_children: false
parent: Navindoor description

---

Simulators are a great tool to improve the design, testing and validation of location systems. That is why we can find different attempts in the scientific community. The following is a summary of some of the existing work in the field, as well as a description of its main characteristics.

SMILe [1] is an open-source simulation tool for developing and evaluating indoor location methods based on propagation time as location metrics, such as Flight Time (ToF) or Arrival Time Difference (TDoA). This tool is based on the OMNET+++ simulator and a Python functionality package for data analysis and processing. SMILe allows the user to configure a space, where several factors can be changed that significantly affect the performance of the location. These factors include the deployment of different nodes, radio capabilities and the inaccuracy of clocks. 

In both Navindoor and SMILe there are tools needed for the design, testing and evaluation of location algorithms from ToF. However, while in SMILe other signals are not yet covered, Navindoor covers a wider range of technologies. Even so, SMILe's ToF signal simulation model is more complex than Navindoor's simulation model.

PyLayers [2] is an open-source radio frequency simulator. It has been designed to evaluate the performance of location algorithms. The radio channel is synthesized using a graph-based ray tracing method. The movement of people is modelled using a virtual force approach. Simulated data can be processed directly with one of the built-in location algorithms or exported to various extensions for external processing.

As in the previous case, PyLayers contains a complex simulator for a specific technology. Although it offers the possibility to process the signals within the simulator itself, it emphasizes the export of its results for external processing. In Navindoor, it is chosen to offer an interface for the incorporation of new simulation models, keeping the whole process in the same development environment.

Sensor Fusion and Tracking Toolbox [3] is a library developed by Mathworks that includes algorithms and tools to design, simulate and analyze systems that merge data from various sensors in order to track the position and orientation of objects. This library includes functionalities for generating trajectories and scenarios, simulating measurements of inertial sensors (accelerometer, gyroscope, magnetometer), GPS receivers, radar, sonar and infrared, different fusion and estimation algorithms (Kalman filters and particle filters), and tools to visualize, analyze and compare the performance of different algorithms.

In this library, as in Navindoor, tools are provided throughout the process of designing location systems. However, in Sensor Fusion and Tracking Toolbox for now only one CLI has been developed, lacking GUI. On the other hand, simulation models in the generation of trajectories are general; they do not simulate a specific asset. In Navindoor the simulation models are focused on the movement of people.

References:
1. Jankowski T, Nikodem M. SMILe – Simulator for Methods of Indoor Localization. 2018 International Conference on Indoor Positioning and Indoor Navigation (IPIN). 2018;(September):24–27. 
2. Amiot N, Laaraiedh M, Uguen B. PyLayers: An open source dynamic simulator for indoor propagation and localization. 2013 IEEE International Conference on Communications Workshops, ICC 2013. 2013;(July 2014):84–88.
3. Mathworks. Sensor Fusion and Tracking Toolbox; 2018. Available from: https://es.mathworks.com/help/fusion/.