---
layout: default
title: Trajectory module
nav_order: 2
has_children: false
parent: Navindoor modules
grand_parent: Navindoor description

---

The objective of this module is to generate trajectories within the created planimetry. The modelling of the trajectories allows to obtain a preview of the behaviour of the algorithms. Motion models take on importance in this module, since the similarity of the results obtained with reality will depend on it.

In Navindoor, trajectories are modeled as a succession of points within the planimetry. These points define the sections through which the asset will move. These can be defined with the help of GUI, simply by doing
click within the planimetry, including plant changes.

Once the points through which the asset will pass have been defined, with the help of simulation models a succession of finer points is generated. This contains coordinates of the points, as well as the corresponding time instant. In this way, velocities and accelerations can be obtained by differentiation. The generation models of the trajectories in our case are focused on the simulation of a person's foot, for which measurements of the foot-mounted inertial systems are simulated using the model proposed in [1]. In addition, in cases of plant changes, a constant velocity model is added.

From the path of the person's foot, the path of the center of masses is generated. This will be used in cases where the sensor is on the trunk of the person. Figure 3 shows the process for generating a trajectory object.

<figure>
  <img src="{{ site.url }}{{ site.baseurl }}/assets/images/ToolDescription/fig3.png" alt="Figure 3. Process of building a trajectory." style="width:100%">
  <figcaption>
    <center/>Figure 3. Process of building a trajectory. In this diagram you can see how the path constructor generates two GroundTruths objects from segments that contain information extracted from the planimetry. In addition, a model is needed that constructs a person's footpath to trav´es from the segments and a model that is capable of creating the path of the center of masses from the path of the foot. The object Ref GroundTruth represents the path of the center of masses, while Foot GroundTruth represents the path of the person's foot.
   </figcaption>
</figure>
<br>
It is important to note that both the simulation models of the footpath and the generation model of the path of the center of masses are optional parameters. That is, the simulation models are independent of Navindoor, so new models can be implemented by creating functions with the same input/output interface as the default functions.

Finally, in the GUI we have tools for the generation of the trajectory, from the option to create a succession of points with clicks, through the creation of new models, to the visualization of the generated trajectory (figure 4).

<figure>
  <img src="{{ site.url }}{{ site.baseurl }}/assets/images/ToolDescription/fig4.png" alt="Figure 4. Capturing an Animation of a Path." style="width:100%">
  <figcaption>
    <center/>Figure 4. Capturing an Animation of a Path. It starts on the fifth and ground floor using different stairs and elevators up to the first floor.
   </figcaption>
</figure>

References:
1. Zampella FJ, Jiménez AR, Seco F, Prieto JC, Guevara JI. Simulation of foot-mounted IMU signals for the evaluation of PDR algorithms. 2011 International Conference on Indoor Positioning and Indoor Navigation, IPIN 2011. 2011.