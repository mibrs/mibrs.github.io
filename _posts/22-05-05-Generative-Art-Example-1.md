---
layout: post
title: "Bring a P5.JS sketch on your post with an iframe tag"
categories: GenerativeArt P5JS
---

### What is this post about?
This post displays a p5.js project from "Generative Gestaltung – Creative Coding im Web". The instructions below 
explain how you can post a p5.js project on your personal blog here on GitHub Pages.

### How to publish your own remix of a p5.js project?
Many different creative projects can be found on [Generative Gestaltung](https://www.generative-gestaltung.de/2/).

#### Prerequisite:
Your GitHub Pages site should be running with Jekyll. A short description on how you achieve this can be found in the Moodle course.

#### Here is a short explanation on what to do.
1. Open the [website](https://www.generative-gestaltung.de/2/), scroll down, then select your preferred project.
2. Open the project in the p5.js editor.
3. Log in to your p5.js account.
4. Duplicate the project in your account (you need to be logged in)
5. Modify the project to your liking.
6. Save your changes.
7. In the menu, open File/Share, click on the first item for creating an iframe tag (Embed option) and copy the content to the clipboard.
8. Open the GitHub repository for your website and navigate to the _posts folder.
9. Create a new post in the folder _posts. In this [post](https://mibrs.github.io/2016/05/20/welcome-to-jekyll.html) you find details on how to do that (format, naming conventions for the file name). Each post begins with a Front Matter detailing information as author name, title of the post, categorisation of the post, ...). Just copy the front matter from another post and modify it.
10. Paste the iframe tag inside your post. You need to add some attributes to the iframe tag, check the code snippet below for details.
11. Make sure that there are empty lines before and after the iframe tag.
12. Commit your changes and refresh your website. It may take up to a minute before the new post is visible.

### Code fragment for the iframe tag
Width and height depend on the canvas size chosen in p5.js. You need to increase the size in iframe to accommodate for the p5.js window inside which your application will run. In the example below, the canvas is 720px x 720px, I have choosen 800px x 800px for the iframe. 

{% highlight html %}
<iframe style="width: 800px; height: 800px; overflow: hidden;"  scrolling="no" frameborder="0" src="https://editor.p5js.org/mikefromd/full/THISCODEISUNIQUEFOREACHPROJECT"></iframe>
{% endhighlight %}


### This is what you should get

<iframe style="width: 800px; height: 800px; overflow: hidden;"  scrolling="no" frameborder="0" src="https://editor.p5js.org/mikefromd/full/zzJHgoQ2D"></iframe>

Now it is your turn to find some interesting animations, remix them and then pubish them on your blog.

