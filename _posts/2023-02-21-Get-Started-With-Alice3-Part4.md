---
layout: post
title: "Get Started with Alice 3 - Part 4"
categories: Introduction Alice-3
author:
- Michael Braehler
---

## Learning Objectives:
- Add and use audio files in projects
- Understand the basic concepts behind events
- Add and use keyboard events and collision detection


## Some remarks

### Audio

[This post](https://kidscoderepo.wordpress.com/2019/12/05/alice-3-audio-files-in-alice/) describes how to upload and use audio clips inside your projects. The Alice website contains an assortment of audio clips that you can download and then use in your projects. You find the folders with the content [here](https://www.alice.org/resources/alice-3-audioibrary/).

Download the folders and then import some resources as shown in the post referred to above and use them with the audio blocks of Alice 3.


### Events (Part 1)

Events are required to allow the viewer of your animation or game made with Alice 3 to interact with your project using keyboard and mouse. As an example, events can be used to control the movements of an object with the arrow keys or the mouse. Furthermore, events are also used inside of Alice for collision detection (objects are recognized and can be made impermeable so that defined objects can not "walk through" the former any more).


#### Example 1 - Person moves and disappears

The project below implements a simple example. There are two eventListeners implemented,
- ```addObjectMoveFor``` allows the viewer to control the position of the object *Person1* by using the arrow keys.
- ```addKeyPressListener``` allow the viewer to make Object *Person1* disappear (Press *1*) or (re)appear (Press *2*) using the opacity property.

![Alice3-Events1](/assets/230221_AliceEvents1.png)


More explanations are given in the Alice 3 How-To Guide that I also uploaded to the [repository for this module](https://github.com/mibrs/Alice3Coding). Download the repository, you find an introduction about Events in part 4 of the handbook.
