---
layout: post
title: "Get Started with Alice 3 - Part 7 - Declare your Own Properties and Procedures"
categories: Introduction Alice-3
author:
- Michael Braehler
---

In particular for games you will also need to create and use properties with your game assets. So you can define a property (variable) that stores if
you have already found a certain asset, for example a coin stack (1). You can also define a counter that collects and adds all points that you
make in a game (2). These two examples are actually already partially implemented in the small game you can download below. I will refer to them
in the following explanations.

First you need to think which object is best to host the property. From the example above, the status of the coin stack belongs to the 
coinStack object, the counter to the person in the game that you are playing and that is collecting the stash.

![How to create a property](/assets/230314_CreateProperty1.png)

Just open the object panel and then click on *add Property* and make entries where the red flash hints at. Once you are finished and have
clicked on ok, the property will be created and two new blocks will appear.

Compared to procedural programming, you will not change the value of the property directy by calling its name, using the assign operator *=*,
followed by its (new) value. In object oriented programming like with Java here, you will use a *setter* procedure to assign a value and a *getter*
function to get its value.

![Property - Setter](/assets/230314_CreateProperty2.png)

The *setter* procedure allows you to assign values to your new property. In the case of the counter, you add a number representing the points 
you want the player to get.

![Property - Getter](/assets/230314_CreateProperty3.png)

The *getter* function allows you to get the value of the property, in our case the number of points saved. You can use this to make maths with it
or simply to print out the value.

So far for the counter, only the property and the setter and getter functions have been implemented. In order for the counter to work, you will 
still need to define a new function that actually adds new points to the existing points you have collected
so far and then call the function at the appropriate locations in the program.

The starter project is available [here](https://github.com/mibrs/Alice3Coding/blob/main/230307%20SimpleGame2.a3p) in this repository, for 
a quick start you can download the project and then remix it. The functionality to prevent assets to be counted more than once is already fully
implemented. Look for the property coinStackTaken, it is true if it is taken, false if it still has not been found.


![class view of TeenPerson](/assets/230321_classOverview.png)

We continue to use the game we have started to build two posts before. In this post we will change the game as follows.

- When the teen comes close to a tree with treasure, there will be a sound and the treasure becomes visible. So the player knows that there is a new treasure close by, but cannot see it yet.
- The player has then to steer the teen so that he can see the treasure.
- Once the treasure is visible for the player, he has to click on it with the mouse. For the mouse handling, we need to create a new event listener. Once the mouse has been clicked, points are added to the teen's counter. Adding points is done with a new procedure ```addPoint```.
- There is mechanism in place so that a treasure can only count once.

First we need to decide where (which class?) to define our new procedure ```addPoint```. As the count property is defined in class ```TeenPerson``` and the count is "belonging' to this person, we create the new procedure there.

Here are the two lines of code required. The procedure uses a parameter ```newPoints```, so we are free to determine the number of points we want to assign. 

![procedure addPoint](/assets/230321_Proc_addPoint.png)

Then we need to add one more listener for the mouse and modify the proximity listener as shown. Now it will only launch a sound when the teen is in proximity (2 meters) of the tree. Everything else, adding the points and blocking the treasure for future attemps to gain points, is handled inside the listener for the mouse.

![Modifications for the Listeners](/assets/230321_ListenerModifs.png)

Now with these features in place, you can further the game as you like by adding more props, treasures, each of them can be assigned points as you like. You always need to modifiy the collision listener, proximity listener and add an additional if statement(s) in the mouse listener. 

For the collision listener it will be enough to add the new object instance to the array, do this by clicking on the *setB* array list and selecting the new objects.

The proximity listener needs a bit more of modification, you need to delete the ```say``` block of the previous version and replace the remaining ```this.tree4``` block in the if block to a ```event getSThingFromSetB``` block. Furthermore, you need to nest two if blocks, then the sound will be played when you are approaching one or the other treasure not yet found.

In the mouseClicked procedure, add one more if statement for each treasure you add using the new treasure (coinStack) instances you have created.

There is another change in the logic of the if blocks, I am using a ```NOT``` with the ```getCoinStackTaken``` function. In this way it is easier to nest the if blocks when you want to add more treasures.

As a simplification, you can also move the ```opacity``` block from the *proximityEntered* procedure to the *mouseClicked* procedure, then you do not need to add if blocks to the former. Try it out! The image below shows you how the changes are implemented. Furthermore, you also need to add ```opacity``` = 0 for the new stash in *myFirstMethod* so that you do not see its location when launching the game.

![Game with two stacks of coints](/assets/230321_ModifTwoStacks.png)

### Video about coding procedures.

The follwing video from the Alice 3 website explains in more detail how to create a procedure.

<iframe 
        width="560" height="315" 
        src="https://www.youtube.com/embed/iFvooPaQBoI" 
        title="YouTube video player" 
        frameborder="0" 
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen>
</iframe>

This seventh session concludes the basic introduction on Alice 3.
