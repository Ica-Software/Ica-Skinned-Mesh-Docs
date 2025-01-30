---
title: Getting Started
nav_order: 2
---


# Getting Started

### To Use Ica Skinner:

- Select your regular SMR in the hierarchy.

- Go to context menu of the SMR Component, and click the
"Setup Ica Skinner".

- If there was no Ica Skinner System in the scene, one will be created.

- Always one and only one System should be exist in the scene, it will be 
users, responsibility ensure that, for example you might make it a child object 
of a manager object that don't unload between scene switches.

- A mesh filter and mesh renderer components will be added to object. 
These are necessary to render the skinned mesh, since Ica Skinner only handle 
the skinning part, does not render itself.

- To change blend shape values, user should use the built in SMR inspector.

- To change other parameters (like materials or shadow casting mode) user
should use the mesh renderer inspector.


### To use Ica Attachment Skinner:

- Add your Attachment model to scene as a child of IcaSkinnedMeshRenderer Component.

- At Mesh Renderer context menu select “Setup Ica Attachment Skinner” 
(similar to IcaSMR).



### To Have Motion Vectors:

To use motion Vectors you need custom shader or modify your existing shader.

- Open your shader in shader graph.

- Import subgraph_FetchMotionVectors to your graph. 

- At "Graph Settings/Surface Options" enable "Add Custom Velocity". 

- Plug the output of subgraph to velocity input of vertex block. 

- On Materials that use that shader, the tick the "Motion Vector for Vector 
Animation" setting.


### In Code

To Get-Set Material: Use Mesh Renderer methods (SetSharedMaterials etc) 
To Get-Set Render Parameters: Use Mesh Renderer methods
To Get-Set Blend Shapes: Use SMR methods