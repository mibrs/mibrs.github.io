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

![Demo Project Tiger](assets/230207_TigerInTheDesert.jpg)

This video shows you a simple example on how you can use these features.

<video width="320" height="240" controls>
  <source src="/assets/230207_Tiger1.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>


## Walking
The code snippets below can be used to make a biped walk. There are two procedures, *firstStep* and *walk*.

*firstStep* brings the biped from the standing position to a walking position. 

[procedure_firstStep](/assets/230207_Tiger_firstStep.png)

*walk* consists on two halfsteps, so the biped finishes
in the same position it started. 

[procedure_walk](/assets/230207_Tiger_walk.png)

In order for the biped to stand properly after walking, we use the built-in procedure *straigtenOutJoints*.

All these methods and some more to show the use of camera and object markers are coded inside the procedure *myFirstMethod*.
![myFirstMethode_Code](/assets/230207_Tiger_myFirstMethod.png)

