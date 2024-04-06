---
layout: page
title: simulating kirigami
permalink: /simulation/onkirigami/
---
<img src="../../assets/images/zippertube.jpg" alt="zipper tube header" width="200"/>

# Simulating Cellular Structures: Kirigami

This work was done in collaboration with my research advisor, Sam Calisch, in the Center for Bits and Atoms (under the direction of Neil Gershenfeld) at MIT.

For this research, I developed workflows that streamlined using two different analysis techniques for folded structures. The first method uses a python framework for Frame3dd, a structural analysis software. Using Frame3dd, I implemented a bar and hinge model that had been proposed to analyze origami structures (Filipov, 2017). Given a geometric input, I used Frame3dd to calculate and visualize stresses, strains, and modal deformations of the folded structure. To streamline the analysis I start from a general file that describes the geometry of the kirigami structure. For this purpose, I use Erik Demaine’s FOLD (Flexible Origami List Data structure) file framework which describes origami models by storing a mesh with vertices, edges, faces, and links between them (Erik D. Demaine, 2016). My python script takes three items as input: 1) a FOLD file with additional arguments for forces and constraints to apply, 2) arguments describing the material properties of folded sheet, and 3) an argument for the bar and hinge model type. Using these parameters, the script is able to simulate the structural response of the folded sheet. Developing this python script involved deconstructing the geometry from the FOLD file into arguments that Frame3dd can understand and also deconstructing the faces of the structure using different bar and hinge models (i.e. 4 nodes-5 bars, 4 nodes-6 bars, 5 nodes-8 bars).

The second workflow I developed uses Abaqus (an industry-standard FEA package) to analyze kirigami structures. Because kirigami structures are planar, this required learning how to work in 2D environments in Abaqus and manipulate planes into three dimensions. To streamline our workflow to simulate using either Frame3dd or Abaqus, I learned to use the python API for Abaqus. This enables me to build geometries without using the graphical interface.

<img src="../../assets/images/zippertube+fold+frame3dd.jpg" alt="zipper tube in different forms" width="900"/>
caption: (left to right): zippertube from FOLD file in Demaine’s Fold Viewer; zippertube created in Abaqus; analysis results of zippertube from Frame3dd

Finally, I developed python scripts to build the FOLD files for a few common kirigami structures: 1) the zipper tube (Filipov, 2017), and 2) the Tachi Miura polyhedron (Tomohiro Tachi, 2012). This involved using an equation relating folding angles in the structure, and developing a method of building the structures modularly so number of units can be used as a parameter in the construction.

This work is still in progress and I hope to continue working with my advisor on a different simulator that uses two dimensional Hermite patches instead of one-dimensional elements or finely discretized grids (as in Frame3dd and Abaqus respectively). More to come!

<img src="../../assets/images/hermitepatch.jpg" alt="hermite patch" width="900"/>
caption: (left to right): Screenshot from Hermite element simulation; curved crease kirigami structure from Hermite patch simulator (from Sam Calisch's Hermite patch simulator: https://calischs.pages.cba.mit.edu/curved_crease_combs/)