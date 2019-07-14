---
layout: default
title: Signal generation module
nav_order: 3
has_children: false
parent: Navindoor modules
grand_parent: Navindoor description

---

In this module, it is possible to simulate different types of signals from the generated path. The objective is to generate data that the localization algorithms will process. As in the previous module, simulation models are crucial for the behavior of the simulator to be true to reality. 
In Navindoor, the abstract Signal class has been created with properties that contain the information of the measurements over a period of time. In addition, two classes have been created that inherit the methods and properties of the class
Signal. These are:
- The BeaconBased class: Representing signals that need access points in order to be simulated.
- The BeaconFree class: Representing signals that can be simulated without the need for access points.

Within the simulation environment, the differences between these classes are seen in the way they are constructed. While the BeaconFree class only needs trajectory information to be defined, the BeaconBased class needs the beacons objects defined in the planimetry module (figure 5).
<figure>
  <img src="{{ site.url }}{{ site.baseurl }}/assets/images/ToolDescription/fig5.png" alt="Figure 5. Representation of signal generation." style="width:100%">
  <figcaption>
    <center/>Figure 5. Representation of signal generation. A diagram of the BeaconFree and BeaconBased signal generation is shown. In addition, the Signal class from which the properties where the measurements will be are inherited is also shown.
   </figcaption>
</figure>
<br>
The BeaconBased class can represent attenuation signals of power level (RSS), arrival angle (AoA) and flight time (ToF), while the BeaconFree class can represent inertial signals (linear accelerations and angular velocities), magnetic field strengths and atmospheric pressure. The default signal simulation models are basic with a Gaussian noise component.

In Navindoor models are treated as input parameters, so it is possible to change them for more complex models simply by creating functions with a specific input/output interface. In the case of BeaconBased classes, the input parameters must be a trajectory point and a beacon object; and the output parameter must be the value of the signal. While in the case of the BeaconFree class, only one point of the path is used as the input parameter and the value of the signal as the output parameter.

On the GUI side, Navindoor has implemented a section for signal generation. This shows a list of previously generated paths. It also shows a selector where you can choose the type of signal you want to generate. For each one of these types it shows a list of the existing models. It also allows us to create new models from a template for each type of signal. In this way inside the GUI we can create several signals quickly, besides visualizing the obtained result.