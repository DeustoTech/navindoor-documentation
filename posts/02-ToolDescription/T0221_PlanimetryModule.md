---
layout: default
title: Planimetry module
nav_order: 1
has_children: false
parent: Navindoor modules
grand_parent: Navindoor description

---

The objective of this module is to characterize the scenario where the experiment takes place. Currently, the trajectories in Navindoor are centred on interior movement, which is why the basic tools are offered to characterise a multi-storey building. This characterization will provide us with information about movement restrictions, position of access points, height between floors, etc. This information can be used by the generation models of trajectories and signals, in addition to the location algorithms.
It has been designed a hierarchy of classes presented in figure 1, which represent the objects necessary for the characterization of a building. The node class has been created to represent a point in three-dimensional space. From this object the other classes are constructed within the planimetry module. The walls objects, which represent the walls of the building, are constructed from two node objects. On the other hand, there are also punctual elements, so classes have been created that inherit the properties of node. These are the objects stairs, elevators, doors and beacons. The objects stairs and elevators indicate the exit points of a plant.
The objects doors, are defined inside the objects walls, and allow the passage in their environment. Finally, beacons represent access points that generate radio signals ˜frecuencia. The objects mentioned above are stored in a class called level in the form of attributes. Finally, a building class has been created which contains a list of level objects in its attributes.

<figure>
  <img src="{{ site.url }}{{ site.baseurl }}/assets/images/ToolDescription/fig1.png" alt="Figure 1. Scheme of the classes." style="width:100%">
  <figcaption>
	<center/>Figure 1. Scheme of the classes. Protruding arrows indicate which class the object is from. While the list inside each box represents the properties that a class contains.
  </figcaption>
</figure>
<br>
For the creation of each of these objects there is a constructor following the bases of object-oriented programming, however the characterization of the planimetry in this way can be very tedious. It is for this reason that
has opted for the development of a GUI (figure 2), which will help us in this work. This way you can define nodes objects with simple clicks, and walls joining nodes objects.
Also the GUI allows to load images, in PNG format, of the planimetry of interest inside the workspace. This can be done for each of the plants so that we can create a faithful reproduction of the planimetry using the real planes as templates. Once constructed the planimetry we can see the building object in 3D, thanks to the GUI options.

<figure>
  <img src="{{ site.url }}{{ site.baseurl }}/assets/images/ToolDescription/fig2.png" alt="Figure 2. Graphical interface for the design of the building planimetry." style="width:100%">
  <figcaption>
    <center/>Figure 2. Graphical interface for the design of the building planimetry. The image shows the interface with a five-storey building. The external figure is a three-dimensional representation of the building. 
   </figcaption>
</figure>