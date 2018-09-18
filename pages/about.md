---
layout: page
title: About
permalink: /about/
---

I am a software product manager based in the Seattle area. Here I am in front of the world's largest oyster:

![Mike in front of the world's largest oyster]({{site.url}}/assets/about/mike-oyster.jpg)

I love outdoors, especially experienced by bicycle.

{% for image in site.static_files %}{% if image.path contains 'assets/about/outdoors' %}<img src="{{ site.url }}{{ image.path }}" alt="{{ image.name | remove: ".jpg" }}" />{% endif %}{% endfor %}

I enjoy reading and writing, especially fiction. Here are some books I have enjoyed:

{% for image in site.static_files %}{% if image.path contains 'assets/about/books' %}<a href="http://www.google.com/search?q={{ image.name | remove: ".jpg" }}"><img src="{{ site.url }}{{ image.path }}" alt="{{ image.name | remove: ".jpg" }}" width="24%" /></a>{% endif %}{% endfor %}

Games and game design are frequently on my mind. [Games can be interesting, fun or both](https://youtu.be/I1Fg76c4Zfg?t=1m21s). I tend to gravitate towards interesting games. Here are some interesting games:

{% for image in site.static_files %}{% if image.path contains 'assets/about/games' %}<a href="http://www.google.com/search?q={{ image.name | remove: ".png" }}"><img src="{{ site.url }}{{ image.path }}" alt="{{ image.name | remove: ".jpg" }}" width="24%" /></a>{% endif %}{% endfor %}

Thank you for visiting my site.