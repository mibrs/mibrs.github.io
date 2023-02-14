---
layout: post
title: "Get Started with Alice 3 - Part 3"
categories: Introduction Alice-3
author:
- Michael Braehler
---

## Learning Objectives:
- Use of the Clipboard and other commands to make facilitate the coding process
- Import (and Export) classes and parts thereof into another class
- How to animate a quadruped
- How to add and use audio files

## Some Explanations

### Use of the Clipboard, Duplicate blocks
The normal copy and paste commands from other applications do not work with Alice 3, the graphical code blocks need 
to be manipulated in a different manner.

Alice has a clipboard, you can see it in the top right corner. You can drag and drop code blocks there. This works
for single code blocks, but you can also drag single code blocks that are part of a conditional (*if then else*), a loop (*while*)
or a structure (*do together*). You cannot select several blocks together and drag them on the Clipbard.

By default, the selected blogs are removed (similar to *Cut* in a normal editor) when you move them to the Clipboard.
When you press the option key on your keyboard while selecting them, they remain on the Code editor. 
You can add more than one code block to the Clipboard.

When you remove (*Paste*) the blocks to your destination, they are by default deleted from the Clipboard. If you want to keep
them there, press the option key while dragging them out of the Clipboard. When you have several blocks of code on the
Clipboard, the oldest will be the last one you can retrieve (Stack).

If you want to duplicate a block in the editor, just press the option key, click the item you want to duplicate and
then drag it to its destination. Then you can release the option Button.


## Import (and Export) classes
![Alice Import Export of Classes](/assets/230214AliceImportExport1.png)

Alice allows you to import classes into your project. Actually when importing into a class of the same name, you get a panel 
highlighting the new procedures, you can then choose which ones to reuse in your project.

![Selection of procedures](/assets/230214ClassImport.png)


## New Procedures for Quadrupeds
In order to get the procedures, please import the class [Quadrupeds.a3c](https://github.com/mibrs/Alice3Coding) by downloading the 
zipped file with the repository Alice3Coding.

In this class you find three new procedures:

### sayWithMouth

### simpleWalk

### sit



## How to Add und Use Audio Files
Everything on how to get audio files into Alice and use them, you can find on the 
[Alice website](http://www.alice.org/resources/how-tos/the-basics-of-using-audio/).

You can also find more sounds to reuse [here](http://www.alice.org/resources/alice-3-audioibrary/).
