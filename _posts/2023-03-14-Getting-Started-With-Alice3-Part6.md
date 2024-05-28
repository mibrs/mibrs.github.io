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


#### Process of Implementation

The game is implmented in two phases.

##### Phase 1 - Described here in Part 6

1. covers creating the  scene,
2. setting camera view,
3. collision detection of the props (except for trash can)
4. proximity detection of trash can
5. some methods opening and closing the lid of the trash can
6. assigning a property, representing each trash piles state (size, depleted, recyclable waste) to each pile
7. Coding some test messages for the above, with ```say``` blocks
 

##### Phase 2 - Described in Part 7 (tbd)

- Keeping track of trash collected
- Keeping track of time elapsed
- Messaging for the user



### Third Person View

Another way for the user to see the player in the game is the **Third Person View**, You bascially see "over the shoulder of the player" and follow his every movements.

![3rd person view](/assets/240515-Set-Camera-3rd-Person-View-1.png)

The view is created in the Set-Up Editor. 

- You create your main character, turn him 180 degrees (0.5) and then fix the camera position with the blue arrows below the screen to your liking.
- Next, you create a Camera Marker for this position, here it is named **camStartPos**. As long as you do not reorient the camera, you will not need it, but if you do, the camera marker gives you the possibility to go back to the original orientation.
- Now, with the Camera object still chosen on the Property Panel, click on ```Vehicle = ``` and then select the name of the Character. This will set up the camera to follow your character later in the game.

The settings you set up in the editor are only valid as long as you do not change the camera position in game with code. The best way to attach the camera permanently for the 3rd player view is to do so in the Code Editor.

The code inside the *sceneActivated* handler is executed first whenever you run your program. with the ```setVehicle``` block you can assign the camera to your character. Before the ```setVehicle```, you should also add a block ```<this.camera> moveAndOrientTo <yourCameraMarker>```. This will move the camera to the assigned position.

![Activiation Listener](/assets/240515-StarterCode-for-3rd-Person-Camera-View.png)

Now you are ready to move your player around the game.


#### Further References

- The video introduces how to create a first person view, but it can easily be modified following the instructions above for a 3rd person view. Furthermore, it also shows you how to code the view and switch in between different views using the key listener. [Alice 3 Setting Up A First Person Camera](https://youtu.be/jxXEXJgrm18?feature=shared)
- This video demonstrates the 3rd person view [Alice 3.1, Camera Movement, tutorial 0.4, Beginner](https://youtu.be/gDlxKxJTW7Y?feature=shared)


### Collision and Proximity Detection

This important concept is implemented with event listeners and handlers. You can define them on the tab ```initializeEventListeners```. The screenshots shown here do not apply to our specfic game, but they are easily transferable.

![Define Listeners](/assets/230307_SelectEventHandlerCollision.png)

You need to declare on two panels which objects can collide/get close to each other. In this case Alf of (setA) should not collide with the trees (in setB). So Alf will appear on one panel, the six trees by name on the other panel.

![SetA panel](/assets/230307_SelectCollisionSetA.png)

![SetB panel](/assets/230307_SelectCollisionSetB.png)


#### Some Explanations to the Code

This is the complete code for the event handlers, the code is explained in the sectios below.

![Park Clean Up Code V1](/assets/240516-ParkCleanUp-V1.png)

##### Event Listeners and Handlers

Most of the coding so far is done in the tab. ```initializeEventListeners```.

There is the ObjectMover that allows you to steer the player with the arrow keys.

The collision and proximity listeners are used to make the game more realistic and allow for more interaction between objects. The code below shows you how the handlers are used in the Park Clean Up. The trees and structures are set up in setB of the collision handler. Whenever the player is approaching one of these obstacles, he is repelled.


##### Trash Piles 

Alice has different types and sizes of trash piles, each of them is actually the same object type, but using different *skins* to make them look different. *Skins* are not a property in Alice, you can only change (*set*) them with a procedure. You cannot *get* information about the skin active.

For the game, we need to know the size and type of trash of each of them. Therefore, we are creating a new property *typeOfTrash* for class *TrashPile* that can hold the following values:

   3 - Large Pile
   2 - Medium Sized Pile
   1 - Small Sized Pile
   0 - Empty, no more trash there
   -1 - Trash not for collection in the game.

![Property tupeOfTrash](/assets/240528-Property-typeOfTrash.png)

The following code is using two arrays and a for ... each loop to set the values for each trash pile instance. This is an advanced, but flexible method. You can also use the out commented block ```<this.trashPile> setTypeOfTrash <typeOfTrask <value>>``` six times, once for each pile. <value> is a whole number taken from the list of 5 values above. Here is the full code.

![Init code for trash piles](/assets/240515-InitTrashPiles.png)


##### Trash Can

When the player *Alf* comes into proximity of the trash can, the method trashCanOpen is called.

![trashCanOpen Method](/assets/240515-TrashCanProcCall.png)

The lid of the trash can is a subpart, this short procedure makes the lid open and close as a short animation.

![Open and close lide of trash can method](/assets/240515-trashCanOpen-Proc-Definition.png)


#### References

The project is also available at [240520 ParkCleanUp1.a3p](https://github.com/mibrs/Alice3Coding/blob/main/240520%20ParkCleanUp1.a3p) as download for this activity.
