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
- Understand the basic concepts behind events (revision), more applications
- How to use the collision listener with Alice 3


### Short Revision on Events, Listeners, Triggers, and Execution of Code

Listeners allow you to trigger the execution of code. Whenever a predefined event on your computer is registered by a listener method, the code associated with that listener is run. What type of events are the listeners looking for? This can be mouse clicks, the key ```c``` is pressed, an object inside your game comes into proximity of another object, and many more. When such an event occurs, the execution of the code inside the particular listening method will be triggered.

So far, we have used the ```addObjectMoverFor ...``` to steer our rover. Furthermore, we have implemented a proximity listener to detect when the rover is within 1 meter distance to some predefined objects on the Mars surface. Check again in part 4 of the series. We just continue here where we left off with the Mars Rover Game before.


### How to execute code before the start or after a defined time

Another classs of events allows us to run code at the beginning of the program or after a certain amount of time after that.is the start of a program. Whenever you click on the ```Run``` button, this triggers the addSceneActivatinnListener to execute some code. The following example makes sure that the camera is always at the starting position.

[Scene Activation Listener](/assets/240515_Alice3_addSceneActivationListener1)




### First Person Mode

Many games are run in the first person mode, the user sees things through the eyes of the acting model. We will continue to expand our small Mars Rover Game we have developed in part 4 of this series. As before, we are dealing with listeners, so we will code inside the tab ```initializeEventListeners```.

![Camera Settings for First Person View with one shots](/assets/230307_SetCameraMarkers.png)

![Code for First Person View](/assets/230307_EventsForFirstPersonView1.png)

[Code for the Listeners](/assets/ )

This simple game has one player, named Alf. You can control the camera view by pressing the keys
- ```C``` Start view
- ```P``` First Person View

You move the person around with the arrow keys. When you approch the magic tree (tree4), he will say *hello* and a pile of coins will appear magically.

If you want to get another view about how to implement the first person camera view, click on [Setting up a First Person Camera](https://youtu.be/jxXEXJgrm18), the link brings you to a video demonstrating everything we have discussed and more.


![Event Tab](/assets/230307_SimpleGame2Events.png)

There is the ObjectMover that allows you to steer the player with the arrow keys. Then the three keys described above allow the player to change the perspective of the camera.


### Collision Detection

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


#### Some Explanations to the Code

The collision and proximity listeners are used to make the game more realistic and allow for more interaction between objects.

![MyFirstMethod](/assets/230307_SimpleGame2.png)

Here is a view on the game. When watching the video and also looking at this image will   notice that the pile of coins is visible. The game was played already one time before I recorded it. Can you suggest a change in myFirstMethod that will correct this error?
![One view at the game](/assets/230307_SimpleGame2Intro.png)

The project is also available on the [Alice repository](https://github.com/mibrs/Alice3Coding) for this activity here on GitHub. You can download (clone) the repository together with other useful information.
