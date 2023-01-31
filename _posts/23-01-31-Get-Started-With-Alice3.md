---
layout: post
title: "Get Started with Alice 3"
categories: Introduction Alice-3
author:
- Michael Braehler
---

## Structure of the sessions
The introduction on Alice 3 follows the free online ebook [Alice 3 - How To Guide](http://www.alice.org/wp-content/uploads/2017/05/Alice-3-HowToGuide-Complete.pdf).
The book is in PDF format, so you can download it and work with it even without Internet connection.

## Here on this post you find additional information and examples that you can use.

### Session 2 covers the first part of Setting Up a Scene, Chapter 2

- How to position, orient, and resize objects (Section 1)
- Adding an object to a scene (Section 2)
- Setting object properties in the Scene editor (Section 3)
- How to set atmospheric properties in a scene (Section 4)
- Positioning sub-parts in Scene editor (Section 7)
- Precise positioning with one-shots  (Section 10)


#### How to use the New Axes object to visualize sub-part / joint movements

When  working with sub-parts, in particular for bipeds, you are faced with a lot of joints and it is difficult to find them and identify their orientation. The
later you need to know in order to move, turn, and roll them.

A trick is to create an instance of the object type *New Axes()* and then link it to the joint you want to explore.

1. Create a new New Axes() object.
2. Go to the Object inspector on the right side and select with "Vehicule" the object or sub-part you want to attach the New Axes object. 
3. As ab alternative to 2., you can also use the  method *moveAndORientTo*. But this will not follow the movements you apply to your joint.
4. You are done, now the axes are attached to the joint, and you can easily predict how to manipulate roll, rotate and other movements. You may resize the axes
before you start your trials. The "one shots" are the perfect tool to define the movements and see immediately what happens.

![Use of instance of New Axes to Visualize joint movements](/assets/230131_Alice_AxisToShowOrientationOfJoint.png)

)

