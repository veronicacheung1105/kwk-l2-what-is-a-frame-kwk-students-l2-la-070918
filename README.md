## Objectives

1. Introduce A-Frame
2. Familiarize yourself with an example scene

## Introducing A-Frame

[A-Frame][a-frame-intro] is a JavaScript framework that allows you to build 3D virtual reality applications that run in the browser. A-Frame leverages an [**Entity-Component-System**][ecs] (ECS) framework. This framework helps us, as programmers, structure our projects and user experiences. The components of the ECS framework are intuitive:
  - **Entity**: a general purpose object (i.e. a shape on the screen)
  - **Component**: an aspect of an object (think: color, position, velocity)
  - **System**: the overarching environment that encompasses entities (i.e. the scene itself, which manages the rendering and animations of entities)

A-Frame is a large library with months of material to master. Consequentially, we don't have time to explore every aspect of it. As a crash course, we will introduce you to some of the basic building blocks with the intention of getting you creating your own custom content quickly.  

## A Simple Scene

In order to make use of the A-Frame library, we are going to be requiring it via a top level `<script>` tag in our html. Take a look at this projects `index.html` and familiarize yourself with the code and identify each of the bullets below:
  - We require the script so that our application has access to the A-Frame library methods and html content
  - Via html **tags**, we are defining several A-Frame **entities** to be rendered
  - Via html **attributes**, we are defining A-Frame **components** (position, geometry, color)
  - Via a wrapper html `<a-scene>` tag, we are defining an A-Frame **system**

Go ahead and start up your local server and take a look at what renders in the browser. An open 3d world and a visual representation of each a-tag within the scene.

## Using the Inspector

A-Frame provides us with an option to use a powerful inspector that comes with the library (similar to Chrome Developer Tools). To open it, use the following command: `ctrl + alt(option) + i`. Everything we can do in the inspector can be done programmatically. It is useful to explore the realtime effects of changing values that exist in our code.

Let's use the inspector now to 'demystify' the sky entity and see how it, like the other shapes you see in the scene, is just another entity:
  - Change the color of the sky entity
  - Shrink the sky (a radius of 10 should do it)
  - Use the access movement arrows (shown as red/blue/yellow arrows) to move the sky so that it no longer encompasses the shapes

This is a straight forward example of an important point when programming visual experiences: we 'trick' the user into believing they are perceiving something with a clever trick. In this case, the sky can be visually interpreted as a boundless blue expanse, while in reality it is a sphere with a solid interior color. If we wanted, we could wrap a 2d image of clouds around the inside of that sphere to further the illusion!

If you like, try replacing the sky **entities** color **attribute** with an image of your choosing. Naturally, we opted to slap [Chrome-Boi][rejected-chrome-boi] into the sky by replacing the entity with the following: `<a-sky src="./assets/chrome-boi.png"></a-sky>`

[rejected-chrome-boi]: "https://en.wikipedia.org/wiki/Draft:Chrome_Boi"
[ecs]: "https://en.wikipedia.org/wiki/Entity%E2%80%93component%E2%80%93system"
[a-frame-intro]: "https://aframe.io/docs/0.8.0/introduction/"
