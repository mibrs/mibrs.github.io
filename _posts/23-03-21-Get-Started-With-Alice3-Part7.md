---
layout: post
title: "Get Started with Alice 3 - Part 7 - Write your own procedures"
categories: Introduction Alice-3
author:
- Michael Braehler
---

In the previous post you learned how to create and use properties. In this post we will write a new procedure that is using the property ```points```.

![class view of TeenPerson](/assets/230321_classOProverview.png)

We continue to use the game we have started to build two posts before. In this post we will change the game as follows.

- When the teen comes close to a tree with treasure, there will only be a sound. Then the player knows that there is a new treasure close by.
- The player has then to steer the teen so that he can see the treasure.
- Once the treasure is visible, the player has to click on it with the mouse. For the moust handling, we need to create a new event listener. Once the mouse has been clicked, points are added to the counter for the teen. Adding points is done with a new procedure ```addPoint```.
- There is mechanism in place so that a treasure can only count once.

First we need to decide where (which class?) to define our new procedure ```addPoint```. As the count property is defined in class ```TeenPerson``` and the count is "belonging' to this person, we create the new procedure there.

Here is the two lines of code required. The procedure uses a parameter ```newPoints```, so we are free to determine the number of points we want to assign. 

![procedure addPoint](/assets/230321_Proc_addPoint.png)

Then we need to add one more listener for the mouse and modify the proxmity listener as shown. Now the proximity listener will only launch a sound when the teen is in proximity (2 meters) of the tree. Everthing else, adding the points and blocking the treasure for future attemps to gain points, is handled inside the mouse click event.

![Modifications for the Listeners](/assets/230321_ListenerModifs.png)

Now with these features in place, you can further the game as you like by adding more props, treasures, each of them can be assigned points as you like. You always need to modifiy the collision listener, proximity listener and add an additional if statement in the mouse listener. For the collision and proximity listener it will be enough to add the new object instance to the array, do this by clicking on the *setB* array list and selecting the new objects.


### Video about coding procedures.

The follwing video from the Alice 3 website explains how to create a procedure in more detail.

<iframe 
        width="560" height="315" 
        src="https://www.youtube.com/embed/iFvooPaQBoI" 
        title="YouTube video player" 
        frameborder="0" 
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen>
</iframe>
