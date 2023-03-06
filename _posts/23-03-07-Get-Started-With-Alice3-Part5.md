---
layout: post
title: "Get Started with Alice 3 - Part 5"
categories: Introduction Alice-3
author:
- Michael Braehler
---

## Learning Objectives:
- Initialize event handlers and what to pay attention to
- Initialize and use mouse events
- Use position and orientation events to introduce collision and proximity detection to your games


## Some remarks

### Audio (Review)

[This post](https://kidscoderepo.wordpress.com/2019/12/05/alice-3-audio-files-in-alice/) describes how to upload and use audio clips inside your projects. The Alice website contains a assortment of audio clips that you can download and then use in your projects. You find the folders with the content [here](https://www.alice.org/resources/alice-3-audioibrary/).


### More About Events

Events are required to allow the viewer of your animation or game to interact with your project using keyboard and mouse. Objects in your scene can
also be used send out an event when another object approaches (proximity) or touches (collision) them. 



#### Example - Person moves along an alley

The project below implements a simple example. There are three eventListeners implemented.
One event handling demonstrates how to use the mouse, clicking moves the character across the scene. Furthermore, the test project demonstrates
proximity and collision detection and how to use it.

More explanations are given in the Alice 3 How-To Guide that I also uploaded to the [repository for this module](https://github.com/mibrs/Alice3Coding). Download the repository, you find an introduction about Events in part 4 of the handbook.
