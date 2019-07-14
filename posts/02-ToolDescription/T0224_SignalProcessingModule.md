---
layout: default
title: Signal processing module
nav_order: 4
has_children: false
parent: Navindoor modules
grand_parent: Navindoor description

---


The objective of this module is to provide the user with basic algorithms for locating the generated signals. These algorithms will be used as a starting point for the design of new ones.

In Navindoor the Extended Kalman Filter (EKF) and the Unscented Kalman Filter (UKF) are implemented. To implement new algorithms it is necessary that they have a specific input/output interface. The algorithms must have three input parameters: The building object, a list of signals generated in all time instants and a structure with all the a priori information of the trajectory. They must also have as output parameter a four-column matrix. The first three columns indicating space and the last column indicating time (figure 6). Navindoor processes this information to create a trajectory object. In this way the estimation will have the properties and methods of the real path.
<figure>
  <img src="{{ site.url }}{{ site.baseurl }}/assets/images/ToolDescription/fig6.png" alt="Figure 6. Input/output interface for location algorithms." style="width:100%">
  <figcaption>
    <center/>Figure 6. Input/output interface for location algorithms. As input it has three variables, the first one representing the planimetry, the second one representing all the previous knowledge about the trajectory and the third one a list of the signals. The algorithm returns a 4 X N matrix, N being the number of measurements.
   </figcaption>
</figure>
<br>
With respect to the GUI, Navindoor shows a list of the trajectories that have been generated. For each of these paths we can see the available signals. In this way we can select the trajectory and the signals.
that we want to process. Since the algorithms have the input/output interface presented above, it is possible to execute them with a single click. Navindoor, after executing the algorithm shows the real trajectory and the estimated trajectory within the loaded planimetry. Also, thanks to the fact that the estimation is a trajectory object, we can use the animation used in the trajectory generation module, giving a real time view of the behavior of the real trajectory versus the estimated trajectory.