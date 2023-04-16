---
layout: post
title: "Get Started with Alice 3 - Part 6 - Properties"
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
