---
layout: default
title: Evaluation module
nav_order: 5
has_children: false
parent: Navindoor modules
grand_parent: Navindoor description

---

The aim of this last module is to compare different estimates of the trajectory. The difference of the executions can be in the algorithm used to estimate, however it can also be in the simulation models of the trajectory, in the simulation models of signals, or simply in the frequency of sampling of some signal. We should note that the estimates in Navindoor are objects trajectories so from the point of view of the code, there is no structural difference between the actual trajectory and the estimate. This makes the comparison between them easier.

In the GUI, Navindoor shows us a list of the generated trajectories, being able to select one of them. For each of these trajectories the available estimates are shown. We can select the estimates we want to compare them in the same graph representing the empirical cumulative distribution function (eCDF), taking as reference the real trajectory. In this way we have a view of the behaviour of the two estimates in the same graph.