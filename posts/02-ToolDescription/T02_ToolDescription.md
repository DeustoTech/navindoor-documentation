---
layout: default
title: Navindoor description
nav_order: 2
has_children: true
---
The methodologies used for the design, testing and validation of localization systems are as varied as the diversity of technologies and techniques used for their implementation. 
However, there are a number of common steps in the design of localization systems. These are: the obtaining of the planimetry, the generation of trajectories, the taking of measurements of signals in this trajectory, the processing of the signals and finally the evaluation of their performance by comparison. The measurements taken should be varied, since a collection of few cases can add unwanted biases to our systems. 
It is therefore necessary to test in various environments, taking measurements in different trajectories. However, obtaining experimental measures of this type are costly in terms of time and resources. 

Consequently, simulation tools are a very interesting alternative. Good simulation models, both in the trajectory and in the generation of signals, can generate a wide range of tests. However, for now there is no standard framework to develop algorithms of various kinds. The few simulators that exist are usually focused on a particular technology, which does not allow comparison with other types of location systems.

This article presents the simulation platform, Navindoor. This is an open source library for MATLAB, where the user can build the planimetry, generate trajectories, simulate signals, develop algorithms, and compare them with others. Navindoor contains a graphical interface (GUI), which facilitates the interaction with the platform. 

In addition, it contains a command line interface (CLI), which facilitates automating voluminous simulations and integration with other tools. Unlike other location system simulation platforms, where simulation models are anchored to the design, this has been developed in a modular way. Due to this, the implementation of new models and algorithms is more versatile. Within Navindoor we can use MATLAB functions as input parameters. In this way developing a simulation model or location algorithm is simplified in creating a MATLAB function, with a specific input/output interface.