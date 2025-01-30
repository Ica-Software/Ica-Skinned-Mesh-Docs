---
title: Attachment Skinner
nav_order: 3
---


# Attachment Skinner
Attach Skinner is a different kind of skinner that can be used on meshes 
that should follow closely some base mesh. For example clothing meshes for 
a character. 

It achieves this by mapping every vertex to closest triangle of 
base mesh. Then whenever base mesh deforms (via bones or blend shapes) it makes
the that vertices the follow the mapped triangles, using barycentric
coordinates. 

Since it does not require any kind of weight or blend shape 
transfer, it significantly simply asset creation pipeline. 
Also its more performant and memory-disk efficient than regular skinning.
 
 But also its more prone to artifacts, specially if attachment mesh vertices
 have high distance to closest base triangle, or when base mesh is low poly
 on some areas. Another limitation of Attachment Skinner is, attachment cannot 
 have custom blend shapes for itself, it can only follow the deformations 
of the base mesh. 
 
Even if these limitations would not work four your project, it can be still 
valuable while development and prototyping.
 
 
 # Usage
 
 Attachment Skinner should be child of the Ica Skinner component.
 
 Unlike Ica Skinner, Ica Attachment Skinner does not require SMR.
 
 All material and render parameter setting change edited via Mesh Renderer
 itself. 
 
 Attachment Skinner also support motion vectors too.
 
