Background
===========

Hexahedral meshing plays a critical role in high-fidelity computational solid mechanics by enabling more accurate and stable simulations, particularly in structural and finite element analyses. Despite its advantages, widespread adoption in industry has been limited due to long lead-time and lack of user friendly tools. 
This user manual introduces a new hex meshin software that leverages the topological sweeping operations to simplify the meshing process. The tool aims to provide an accessible, efficient, and high-quality user experience, particularly for engineers and researchers who may be unfamiliar with traditional hex meshing techniques. Hexehedral meshing demonstrates numerous benefits, however, many exisiting tools require specific geometric conditions and have steep learning curves.
To address these challenges, the softare uses a sweeping algorithm that divides geometry into similar cross-sections. A hex mesh is first generated on a 2D cross-section and then projected through the volume from one section to the next. This method enhances both efficiency and adaptability, with the swept object defined by its traces and level sets as described below:

i. Traces: Traces are path lines that traverse each cross-section of the geometry. They must intersect every level set. The number and placement of traces can be customized within the algorithm to best suit the geometry being meshed.  

   .. figure:: _static/Traces_Background.png 
      :alt: Image of traces through a basic geometry. These traces are viewed in Paraview. 
      :align: center
      :width: 275px
      
ii. Level Sets: Level sets are discrete slices of the cross-section placed at regular intervals along the sweep path. These sections serve as anchoring points for projecting the mesh. Like traces, the number and position of level sets are configurable within the algorithm. 

   .. figure:: _static/LevelSets_Background.png
      :alt: Image of level sets of a basic geometry. These level sets are viewed in Paraview. 
      :align: center
      :width: 275px
