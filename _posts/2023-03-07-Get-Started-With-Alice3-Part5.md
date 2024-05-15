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

Another classs of events allows us to run code jsut at the beginning of the program or after a certain amount of time. Whenever you click on the ```Run``` button, this triggers the addSceneActivationListener to execute some code. The following example makes sure that the camera is always at the starting position when you start the game.

![Scene Activation Listener](/assets/240515_Alice3_addSceneActivationListener1.png)


### First Person Mode

Many games are run in the first person mode, the user sees things through the eyes of the acting model. We will continue to expand our small Mars Rover Game we have developed in part 4 of this series. As before, we are dealing with listeners, so we will add the following code inside the tab ```initializeEventListeners``` by creating a new listener first and then adding the logic.

![Code for First Person View](/assets/240515_KeyPressed_Event.png)

This simple game has one player, that is our Mars rover. We have two views for the camera that can be selected by pressing keys.

- ```C``` Start view
- ```P``` First Person View

If you decide to use more keys to add more features, make sure that you nest the if statements into each other as it is done here for the two keys.

![View of the spaceship as seen from the rover](/assets/240515_FirstPersonView.png)


#### Details for Triggering Keyboard Events

Above the procedure for the keyboardListener there is an option box with ```add detail``` that allows you to configure the listener's response if you press your key(s) many times or longer. 

The options under **multipleEventPolicies** give you choices on how the triggered code should be executed. You have the options of

1. **Enqueue** -> The events are queued and executed one after the other until the queue is empty.
2. **Ignore** -> only one event once (default)
3. **Combine** -> the program will try to execute all at the same time.

The options under **heldKeyPolicy** cover the event handling from the point of view of the trigger. The default option ```FIRE_MULTIPLE``` will keep sending out triggers as long as you keep the key pressed. This is the type of behaviour you would use for a steady movement.

![keyHeldPolicy Options](/assets/240515_keyTriggering.png)

These two settings are influencing each other, so for the default setting all events following the first are ignored due to multiple event setting, but the chosen key policy you allows a steady flow of triggers, as long as you keep the key pressed. Too many triggers and processing in the event loops can deteriorate the performance, and your game may react sluggish.


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
