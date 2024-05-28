---
layout: post
title: "Get Started with Alice 3 - Part 6 - Game Design, Setup, 3rd person view, More Event Listeners"
categories: Introduction Alice-3
author:
- Michael Braehler
---

## Game Design, Set-up, 3rd Person View and More Event Listeners

### Learning Objectives:

- How to design a game?
- 3rd person camera perspective, save start settings
- Use of activation and collision listeners and handlers
- Create a basic game's mechanics

### Game Design

This [video](https://youtu.be/I11Qox6vILg?si=Ywy-_0rXghKbwiyB) describes one process for creating your own games. It uses Alice 3 as its authoring tool, towards the end of the video it specifically introduces you how to code some universal patterns that many games contain.


### The Game Park Clean Up - General Description

#### Description

The game is about doing a cleaning up of a park after a party. The player has to bring the trash from whereever it is in the park to the trash can. He  can only carry a limited amount of trash every time, so he has to travel several times if the trash pile is too big. Furthermore, he can only put recyclable trash into the bin, other types of waste he has to leave for someone else to take care of.

The player has to do the clean up as quickly as possible.


#### Layout of the Game

The cameral view shows you from above the layout of the game.

![Layout of the Game](/assets/240515-TopView-GamePlan-Bin-Circled.png)


#### The Resources Used in the Game

All settings at the beginning of the game are shown on the tab **Scene**. 

![Settings for the game](/assets/240528-Settings.png) 


### Third Person View

Another way for the user to see the player in the game is the **Third Person View**, You bascially see "over the shoulder of the player" and follow his every movements.

![3rd person view](/assets/240515-Set-Camera-3rd-Person-View-1.png)

The view is created in the Set-Up Editor. 

- You create your main character, turn him 180 degrees (0.5) and then fix the camera position with the blue arrows below the screen to your liking.
- Next, you create a Camera Marker for this position, here it is named **camStartPos**. As long as you do not change the camera position later, you will not need it, but if you do the cameral marker gives you always the possibility to go back to the beginning.
- Now, with the Camera object still chosen on the Property Panel, click on ```Vehicle = ``` and then select the name of the Character. This will set up the camera to follow your character when later you move it around in the game.

The settings you fix in the set-up editor are only valid as long as you do not change the camera position in game with code. The best way to attach the camera permanently for the 3rd player view is to do so in the game.

The code inside the *sceneActivated* handler is executed first whenever you run your program. with the ```setVehicle``` block you can assign the camera to your character. Before the ```setVehicle```, you should also add a block ```<this.camera> moveAndOrientTo <yourCameraMarker>```. This will move the camera to the assigned position.

![Activiation Listener](/assets/240515-StarterCode-for-3rd-Person-Camera-View.png)


#### Further References

- The video introduces how to create a first person view, but it can easily be modified following the instructions above for a 3rd person view. Furthermore, it also shows you how to code the view and switch in between different views using the key listener. [Alice 3 Setting Up A First Person Camera](https://youtu.be/jxXEXJgrm18?feature=shared)
- This video demonstrates the 3rd person view [Alice 3.1, Camera Movement, tutorial 0.4, Beginner](https://youtu.be/gDlxKxJTW7Y?feature=shared)


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

![MyFirstMethod](/assets/230307_SimpleGame2.png)

Here is a view on the game. When watching the video and also looking at this image will   notice that the pile of coins is visible. The game was played already one time before I recorded it. Can you suggest a change in myFirstMethod that will correct this error?
![One view at the game](/assets/230307_SimpleGame2Intro.png)

The project is also available on the [Alice repository](https://github.com/mibrs/Alice3Coding) for this activity here on GitHub. You can download (clone) the repository together with other useful information.
