---
layout: post
title: "Get Started with Alice 3 - Part 4 - Input, EventListeners, and the Beginnings of Mars Rover"
categories: Introduction Alice-3
author:
- Michael Braehler
---

## Learning Objectives:
- How to create variables and assign them values
- How to get user input with requester
- Understand the basic concepts behind events and what events Alice can deal with
- Try out your knowledge on a Game of Mars Rover, Part 1


## Variables, Assignments, and Input

The project below is very simple, the man is asking the woman how many dogs she has, this continues until the man guesses the correct number (2). By keeping this game short, you can learn the basics of some key programming concepts without getting lost in a maze of code.

![Project with Variable, Assignment, Input, Loop and Conditional](/assets/2024-05-13_22-52-412.png)

This small project contains all the basics you need for a small interactive program. While the ```say``` blocks come from the persons' procedures, ```variable```, ```assign```, ```while```, and ```if``` can be found at the bottom of the window. Just drag and drop them on the code window and then unfold the options to design your statements. Here are some further remarks.


#### 1. Declare and initialize a variable

Drag and drop a variable placeholder from the bar below to the coding panel. Then this window will pop up.

![Declare and initialze a variable](/assets/2024-05-13_23-12-34.png)

Follow the three numbered steps required to set up your variable

1. Chose its type, mostly it will be one of the four basic data types.
2. Give your variable a name, so that you can later address it.
3. Give your variable an initial value to start with.


#### 2. Assignment

While your program is running, the variable will often change its value. This you do with the assignement operator. On the left of the ```=``` is the name of the variable that will change its value, on the right you put the new value. Often, when you are creating an assignment, in the beginning you will put a placeholder of the proper type at the right side of the ```=``` sign. Later, you will then drag and drop a function with matching output data type on the right side of the assignment.

Be aware that Java is very picky with data types for assigning and applying operations to values. They must have same or "similar" types. In case you cannot drag and drop a value or a function on a field, this is a hint, that there is a type mismatch.


#### 3. Input

The input of values is implemented as functions, one function for every data type you can input (decimal numbers, whole numbers, boolean values (YES or NO, True or False), and text (Strings). In order to use them, first create an assignement for a variable you created earlier of matching type for your input function, then drag and drop the input function ```get...FromUser``` on the right side of your assigment (2).


#### 4. and 5. while loop and conditionals with if

These elements are also dragged and dropped on the coding panel. First, you will just select a ```true``` or ```false``` constant, once the block is fixed, you click through and assemble your logic. All variables that you have created beforehand, are also visible, so you can select them where necessary.


## About Events

### An introduction to event handling

All program code we have done so far is executed as described in the procedure **myFirstMethod**. While this main method uses procedures, functions, and properties from all over Alice, they are executed statically, one after the other, as described in said method. So far we have not seen any way to interfer in this predfined execution. While this may be ok as long as we only want to tell a story, this is not acceptable any longer if we want to create a game. The user needs to interact with the game using the keyboard or mouse, and we may even have some interaction of game objects with each other at an unforseen moment, maybe due to the user's intervention.

Alice uses so called **Eventlisteners** for various types of events. These routines are always listening in to discover predefined events (mouse clicks, begin of program, colliding objects, ...). There are several different types of Listeners you can initialize that discover different types of events. In case a particular Listener notices an event of the type it monitors happening, you can create code that will react to that particular event. This is code is then run outside of the myFirstMethod, maybe in parallel.

Here are two examples.

If you have set up a Listener for the arrow keys on the keyboard, and the user is pressing the up key, you could program your main character in the game to move forward. You can also make your main character stop if he collides with a prefined object in the game. 

In this session we will focus on movements with the arrow keys and the basics for proximity detection to create a small game.


#### Example 1 - Person moves and disappears

The project below implements a simple example. There are two eventListeners implemented,
- ```addObjectMoveFor``` allows the viewer to control the position of the object *Person1* by using the arrow keys.
- ```addKeyPressListener``` allow the viewer to make Object *Person1* disappear (Press *1*) or (re)appear (Press *2*) using the opacity property.

![Alice3-Events1](/assets/230221_AliceEvents1.png)


More explanations are given in the Alice 3 How-To Guide that I also uploaded to the [repository for this module](https://github.com/mibrs/Alice3Coding). Download the repository, you find an introduction about Events in part 4 of the handbook.
