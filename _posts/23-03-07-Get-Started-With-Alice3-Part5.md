---
layout: post
title: "Get Started with Alice 3 - Part 5 - More About Events"
categories: Introduction Alice-3
author:
- Michael Braehler
---

## First Person Mode and Collision/Proximity Events

### Learning Objectives:

- What is a First Person View, implement it in Alice 3 using camera markers and the vehicle block
- Understand the basic concepts behind events (revision)
- How to use collision and proximity listeners with Alice 3


### First Person Mode

Many games are run in the first person mode, the player sees things through the eyes of the acting chararcter. The following link brings you to a video demonstrating how to set up a first person camera mode using the vehicle feature. [Setting up a First Person Camera](https://youtu.be/jxXEXJgrm18). The video first (0:00 to 1:27) demonstrates the technique used with *one shots* in the property panel. The camera is attached to the head of the person, the head serves as vehicle for the camera. 

![Camera Settings for First Person View with one shots](/assets/230307_SetCameraMarkers.png)

Then afterwards (1:27 to end) the technique is implemented in the code editor.

![Code for First Person View](/assets/230307_EventsForFirstPersonView1.png)

The first person view is also implemented in the example for this blog.


### Collision and Proximity Detection

This important concept is implemented with event listeners. You can define them on the tab ```initializeEventListeners```.

![Define Listeners](/assets/230307_SelectEventHandlerCollision.png)

You need to declare on two panels which objects can collide/get close to each other. In our case for the game descibed below, Alf should not collide with the trees. So Alf will appear on one panel, the six trees by name on the other panel.

![SetA panel](/assets/230307_SelectCollisionSetA.png)

![SetB panel](/assets/230307_SelectCollisionSetB.png)

For how to use the event listeners, have a look in the example.


### Game Study with Event Detection

<div style="padding:75% 0 0 0;position:relative;">
  <iframe src="https://player.vimeo.com/video/805407827?h=f1ea515f41&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="GameStudy1Alice.mp4"></iframe>
</div>
<script src="https://player.vimeo.com/api/player.js"></script>

This simple game has one player, named Alf. You can control the camera view by pressing the keys
- ```C``` Start view
- ```M``` See the magic tree
- ```P``` First Person View

You move the person around with the arrow keys. When you approch the magic tree (tree4), he will say *hello* and a pile of coins will appear magically.


#### Some Explanations to the Code

Most of the coding takes place in the tab. ```initializeEventListeners```.

![Event Tab](/assets/230307_SimpleGame2Events.png)

There is the ObjectMover that allows you to steer the player with the arrow keys. Then the three keys described above allow the player to change the perspective of the camera.

The collision and proximity listeners are used to make the game more realistic and allow for more interaction between objects.

![MyFirstMethod](/assets/230307_SimpleGame2)

Here is a view on the game. When watching the video and also looking at this image will   notice that the pile of coins is visible. The game was played already one time before I recorded it. Can you suggest a change in myFirstMethod that will correct this error?
![One view at the game](/assets/230307_SimpleGame2Intro.png)

The project is also available on the [Alice repository](https://github.com/mibrs/Alice3Coding) for this activity here on GitHub. You can download (clone) the repository together with other useful information.
