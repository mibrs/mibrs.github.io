---
layout: post
title: "Get Started with Alice 3 - Part 3"
categories: Introduction Alice-3
author:
- Michael Braehler
---

## Learning Objectives:
- Use of the Clipboard and other commands to facilitate the coding process
- Import (and Export) classes and parts thereof into another class
- How to animate a quadruped
- How to add and use audio files

## Some Explanations

### Use of the Clipboard, Duplicate blocks
The normal copy and paste commands from other applications do not work with Alice 3, the graphical code blocks need 
to be manipulated in a different manner.

Alice has a Clipboard, you can see it in the top right corner. You can drag and drop code blocks there. This works
for single code blocks, but you can also drag multiple code blocks that are part of one conditional (*if then else*), loop (*while*)
or structure (*do together*). You cannot select several blocks together and drag them on the Clipbard in one move.

By default, the selected blogs are removed (similar to *Cut* in a normal editor) when you move them to the Clipboard.
When you press the option key on your keyboard while selecting them, they remain on the Code editor. 
You can add more than one code block to the Clipboard, one after the other.

When you remove (*Paste*) the blocks to your destination, they are by default deleted from the Clipboard. If you want to keep
them there, press the option key while dragging them out of the Clipboard. When you have moved several blocks of code on the
Clipboard, the oldest will be the last one you can retrieve (Stack).

If you want to duplicate a block in the editor, just just press the option key, click the item you want to duplicate and
then drag it to its destination. Then you can release the option key.


## Import (and Export) classes
![Alice Import Export of Classes](/assets/230214AliceImportExport1.png)

Alice allows you to import classes into your project. Actually when importing into a class of the same name, you get a panel 
highlighting the new procedures, you can then choose which ones to reuse in your project.

![Selection of procedures](/assets/230214ClassImport.png)


## New Procedures for Quadrupeds

The following video clip shows you a sample project using tree new procedures to animate a quadruped.

<video width="320" height="240" controls>
  <source src="/assets/230214talkingWalkingFox.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

The code of the main function is straigt forward, it uses the three procedures and changes the camera angle.

![myFirstMethod](/assets/230214_Quadruped_myFirstMethod.png)

In order to get the procedures, please import the class [Quadrupeds.a3c](https://github.com/mibrs/Alice3Coding) by downloading the 
zipped file with the repository Alice3Coding, and then clicking on the Import button inside the Quadruped class.

In the file you get three new procedures highlighted:

### sayWithMouth

![Quadruped_sayWithMouth](230214_Quadruped_sayWithMouth.png)

The procedure animates the mouth while speaking. The procedure introduces a new feature, a parameter. In this procedure, you assign the parameter the text you want to appear in the speech bubble.

### simpleWalk

![Quadruped_simpleWalk](230214_Quadruped_simpleWalk.png)

This procedure coordinates the movements of the four legs to make it appear as the animal is walking. The movement is a simplification, but
it is a good starting point.

### sit

[Procedure sit](/assets/230214_Quadruped_sit.png)

This procedure lets the animal sit down, also taking care of the tail.


## How to Add und Use Audio Files
Everything on how to get audio files into Alice and use them, you can find on the 
[Alice website](http://www.alice.org/resources/how-tos/the-basics-of-using-audio/).

![Alice Website, Content about Audio](230214AliceSiteOnAudio.png)

You can also find more sounds to reuse [here](http://www.alice.org/resources/alice-3-audioibrary/).
