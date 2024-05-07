---
layout: post
title: "Get Started with Alice 3 - Part 2 - Camera and Object Markers, Code Your Own Procedures"
categories: Introduction Alice-3
author:
- Michael Braehler
---

## Learning Objectives
The focus in this session is on 
- getting a better grip on how to move sub-parts and
- using object and camera markers.


## The Tiger in the Desert

![Demo Project Tiger](/assets/230207_TigerInTheDesert.jpg)

This video shows you a simple example on how you can use these features.

<video width="320" height="240" controls>
  <source src="/assets/230207_Tiger1.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>


## Object and Camera Markers

![Tiger with Object Marker](/assets/230207_Tiger_CloseWIthObjectMarker.png)

Alice allows to set Object and Camera Markers. Both type of markers allow you to fix positions on the scene that you can use to move objects to. 

The camera marker allows to you to define camera positions, including orientation/viewing angle. You can save each location with a coloured marker and a name for use in your code. The videos [Camera Markers](https://www.alice.org/resources/how-tos/using-camera-markers/) and [Camera and Object Markers](https://youtu.be/hqE15vsLtAA) show you in detail how to fix and use the camera markers. The block ```<this.camera> moveAndOrientTo <this.aDefinedCameraPosition>``` is the standard block to move the camera in your program. 

Object markers are similar, they allow you to define and save a marker for a location on you scene. This is useful if you want to move an object to a well defined position at another object, for example the top of a stone. You can move without object marker one object to the stone, but this will result in your object to be in the middle of the stone. You need an object marker to pinpoint the top of the stone or any other detailed location, then you can move there. The video here [Bill Barnum: Alice 3 Tutorial - #05 - Object Markers And Camera Markers](https://youtu.be/hqE15vsLtAA?si=lFcWJszvZZc07vPY) describes a scenario with both camera and object markers and how to code them for a short animation.

![Video about how to use camera and object markers](/assets/2024-05-07_09-18-58.png)


## Walking

The three code snippets below can be used to make a biped walk. In order to be able to use the methods not only for the tiger, but for all bipeds, we are defining two procedures in class Biped. One way to create those proecedures is by opening the object tree browser, selecting the Biped class and then clicking on *New Procedure*. The screenshot shows you how to access the part of the code editor that allows you to create and edit procedures and functions.

![How to edit methods](/assets/2024-05-07_09-32-44.png)

The whole process is described in an older tutorial [here](https://kidscoderepo.wordpress.com/category/programming-language/alice/), the method *walk* in that post is slightly different, the method shown below is simpler.

You will need to create two procedures, *firstStep* and *walk*.

*firstStep* brings the biped from the standing position to a walking position. 

![procedure_firstStep](/assets/230207_Tiger_firstStep.png)

*walk* consists on two halfsteps, so the biped finishes
in the same position it started. 

![procedure_walk](/assets/230207_Tiger_walk.png)

In order for the biped to stand properly after walking, we use the built-in procedure *straigtenOutJoints*.

These three methods and some more to show the use of camera and object markers are used inside the procedure *myFirstMethod*. You can also download the project from the repository, it's name is *240506_Tiger3.a3p*. Download the program, remix it and make it your own.

![myFirstMethode_Code](/assets/2024-05-07_11-18-15.png). 

The video at the beginning of this post is the full animation.

The walking algorithm used here is very basic, but this is on purpose as it makes coding faster. The code snippet below places the *walk* method inside a count loop, so the tiger takes 1 + 6 half steps, forth and back.

![Walking only](/assets/220207_TigerWalkOnly.png)

There are more realistic procedures for walking available [here](https://www.alice.org/resources/how-tos/biped-walk-cycle/), you may have a look ahead of next session if you like. 

Furthermore, there is a very comprehensive tutorial on sub-parts/joint movements on the Alice 3 website, [here](https://www.alice.org/resources/how-tos/manipulating-biped-joints/) is the link to the page.



