---
layout: post
title: "Get Started with Alice 3 - Part 5 - More About Events"
categories: Introduction Alice-3
author:
- Michael Braehler
---

## Mouse Events and Collision/Proximity Events

### Learning Objectives:

- What is a First Person View, implement it in Alice 3 using camera markers and the vehicle block
- Understand the basic concepts behind events (revision)
- How to use mouse events to control objects
- How to define collision and proximity events inside Alice 3


### First Person View

Many games are run in the first person mode, the player sees things through the eyes of the acting chararcter. The link brings you to a video demonstrating how to set up a First Person Camera view using the vehicle feature. [Setting up a First Person Camera](https://youtu.be/jxXEXJgrm18). The video first (0:00 to 1:27) demonstrates the technique used with *one shots* in the property panel. The camera is attached to the head of the person, the head serves as vehicle for the camera. 

![Camera Settings for First Person View with one shots](/assets/230307_SetCameraMarkers.png)

Then afterwards (1:27 to end) the technique is implemented in the code editor.

![Code for First Person View](/assets/230307_EventsForFirstPersonView1.png)

The first person view is also implemented in the example 2 for this blog.

