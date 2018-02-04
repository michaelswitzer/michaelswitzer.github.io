---
layout: page
title: About
permalink: /about/
---

* TOC
{:toc}

## Bio
I am a software product manager based in the Seattle area. Here I am in front of the world's largest oyster:

![Mike in front of the world's largest oyster]({{site.url}}/assets/about/mike-oyster.jpg)

I love outdoors, especially experienced by bicycle.

<p>{% for image in site.static_files %}{% if image.path contains 'assets/about/outdoors' %}<img src="{{ site.url }}{{ image.path }}" alt="{{ image.name | remove: ".jpg" }}" />{% endif %}{% endfor %}</p>

I enjoy reading and writing, especially fiction. Here are some books I have enjoyed:

<p>{% for image in site.static_files %}{% if image.path contains 'assets/about/books' %}<a href="http://www.google.com/search?q={{ image.name | remove: ".jpg" }}"><img src="{{ site.url }}{{ image.path }}" alt="{{ image.name | remove: ".jpg" }}" width="24%" /></a>{% endif %}{% endfor %}</p>

Games and game design are frequently on my mind. [Games can be interesting, fun or both](https://youtu.be/I1Fg76c4Zfg?t=1m21s), and I tend to gravitate towards interesting games. Here are some interesting games:

<p>{% for image in site.static_files %}{% if image.path contains 'assets/about/games' %}<a href="http://www.google.com/search?q={{ image.name | remove: ".png" }}"><img src="{{ site.url }}{{ image.path }}" alt="{{ image.name | remove: ".jpg" }}" width="24%" /></a>{% endif %}{% endfor %}</p>

Thank you for visiting my site.

## FAQ
### Can I use your content?
Unless specifically specified, I own all of the content on this site; it is copyright Michael Switzer. You do not need to ask me before linking to this site, but please do not leech my images or copy my work anywhere else. If you have any specific inquiries about this, feel free to reach out through the contact links below.

### How did you make this site?
I use [Jekyll](https://jekyllrb.com) to generate static pages, which I host for free on [github pages](https://pages.github.com/). I happen to like the default theme for Jekyll, [minima](https://github.com/jekyll/minima), so I use a lightly adapted version for this site. The source code is freely available at my [github](https://github.com/michaelswitzer/michaelswitzer.github.io).

### Are you available for hire?
I am currently employed but happy to connect if you think I might find the opportunity exciting. Feel free to shoot me an email or contact me via LinkedIn/AngelList. I am not interested in relocating at this time though that could change in the future.