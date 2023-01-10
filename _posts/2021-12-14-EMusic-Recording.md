---
layout: post
title: "How to record and publish audio clips"
categories: audio web-design
---

### What we did

During this session we made an audio recording. We were using [Learning Music](https://learningmusic.ableton.com/) as a sound source and recorded a short music clip with Audacity. Here is a screenshot of what we did.

![Image Learning Music and Audacity](/assets/211130AudacityRec1.png)

At the end we were converting the original wav file into the more compact mp3 format and published the audio file on a website. This is the code we were using for that:

{% highlight html %}
<div>
  <audio controls>
    <source src="/assets/intro1.mp3" type="audio/mpeg">
  </audio>
</div>
{% endhighlight %}

### Here is the audio clip:

<div>
  <audio controls>
    <source src="/assets/intro1.mp3" type="audio/mpeg">
  </audio>
</div>
  

