---
title: "Blender Cloth Napkin Tutorial"
date: 2021-03-14T09:48:30+03:00
draft: false
---
This Blender video demonstrates how to make an image of a cloth napkin draped over a glass cup. 
Blender's cycles render engine is used during this video. Blender version 2.68a was used for this tutorial. 
This video shows many techniques that may be helpful to beginners.This Blender video demonstrates how to 
make an image of a cloth napkin draped over a glass cup. Blender's cycles render engine is used during this 
video. Blender version 2.68a was used for this tutorial. 

This video shows many techniques that may be helpful to beginners.

I will be doing this tutorial with using the keyboard hot keys as possible to eliminate the use of the
mouse as much as possible.

## Genral Hot Keys

### Change Views

* Left    Ctrl+Num3
* Right   Num3
* Back    Ctrl+Num1
* Front   Num1
* Bottom  Ctrl+Num7
* Up      Num7
* Toggle Selecting/Deselecting Everything  A/Ax2
* Selecting Vertices by drawing a box around them  B
* Delete  X
* Scale S -> Z -> 0

## Modelling

### Change rendering engine to cycles render

Cycles is Blender's physically-based path tracer for production rendering. 
It is designed to provide physically based results out-of-the-box, with artistic control
and flexible shading nodes for production needs.

* Go to Render Properties Evee > Cycles Render

### Delete Cube

* X > Enter to Delete

### Cup

* Shitf+A > Mesh > UV Sphere

* Zoom in and out +/- keys

#### Convert sphere to glass cup

* Ctrl+Tab  - Change from Object mode to Edit mode 

* Z  - View port shading options > Wireframe.

* 5  - Orthographic projection.

* Num1 - Front View.

* A/Ax2 - Select/Deselect everything.

* B Key to select vertices by drawing a box around them.

* X to Delete Vertices

* For the bottom section of the sphere Press B to select vertices, S for scale then Z to 
restrict to Z axis then enter 0 as the value then hit enter.

* Z > 6 To Change from Wireframe to Solid

* Ctrl+Tab to return to Edit Mode.

#### Add Thickness to Cup

* Add Solidify Modifier - Thickness 0.07

* Smooth the surface of cup - Add a Subdivision Surface Modifier - Levels 2, Render 2, Then Object > Shade > Smooth.

* Add Material and set surface to Glass BSDF

### Plane

* Shift+A to Add Plane

* S to Scale then 5 then Enter Key

* Num 1 to Switch to Front View

* G > Z To Move plane to bottom of cup

#### Plane Material

* Material: Diffuse BSDF

* Color: White

### Cloth Napkin

* Shift+A to Add Plane

* S > 5 > Enter

* Rotate R > Z > 45 > Enter

* R > X > 70 > Enter

* Num 3 > G > X Then move

* Num 3 > G > Z Then move

#### Napkin Material

* Material Type: Glossy

* Roughness: 1.00

* Color: Blue

* Settings > View Port Color : Blue

* Ctrl+Tab for Edit Mode

* A/Ax2 Multiselect

* Edge > Subdivide > Cuts: 50

* Ctrl+Tab for Object Mode

#### Napkin Modifiers

* Add Cloth, Solidify and Subdivision Surface Modifiers

* For Surface Modifier, View and Render : 2

* Object > Shade > Smooth

* Physics > Cloth > Cotton

* Quality Steps: 10

* Check Cloth Collision and Self Collision to allow self interaction

* For Cup and Bottom Plane, click and select collision.

