---
layout: post
title: "Get Started with Alice 3 - Part 2"
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

Alice allows to set Object and Camera Markers. Both type of markers allow you to fix positions on the scene that you can use to move objects to. Details on how to use [Camera Markers](https://www.alice.org/resources/how-tos/using-camera-markers/) and [Camera and Object Markers](https://youtu.be/hqE15vsLtAA) you find in these two videos.

## Walking
The code snippets below can be used to make a biped walk. There are two procedures, *firstStep* and *walk*.

*firstStep* brings the biped from the standing position to a walking position. 

![procedure_firstStep](/assets/230207_Tiger_firstStep.png)

*walk* consists on two halfsteps, so the biped finishes
in the same position it started. 

![procedure_walk](/assets/230207_Tiger_walk.png)

In order for the biped to stand properly after walking, we use the built-in procedure *straigtenOutJoints*.

These three methods and some more to show the use of camera and object markers are used inside the procedure *myFirstMethod*.
![myFirstMethode_Code](/assets/230207_Tiger_myFirstMethod.png). The video at the beginning of this post is the full animation.

The Walking procedures are basic so that you can implement them quickly. There are more realistic procedures available [here](https://www.alice.org/resources/how-tos/biped-walk-cycle/), you may have a look ahead of next session if you like. 

Furthermore, there is a very comprehensive tutorial on sub-parts.joint movements on the Alice 3 website, [here](https://www.alice.org/resources/how-tos/manipulating-biped-joints/) is the link to the page.



