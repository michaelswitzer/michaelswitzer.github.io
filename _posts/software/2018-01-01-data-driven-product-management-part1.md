---
layout: post
title:  "Data-driven Product Management Part 1"
permalink: /software/:year/:month/:day/:title.html
date:   2018-01-01
type: Software
summary: We explore Waterfall development strategies and give a brief overview of how the world looked before big data.
---

## It's my first post!

For the beginnings of this blog, I thought I would write a high-leveled introduction to what I consider the most important conceptual framework that drives product development today: Data-driven decision making (DDDM). Even for non-tech folks, understanding the basics of DDDM and how it is used to build products can help you protect yourself as a consumer and understand how companies like Amazon, Google and Microsoft manage to maintain high standards of quality even as their companies scale considerably year over year.

For anyone currently in a product management role, understanding the intricacies of DDDM can mean the difference between a decent product and a hugely successful one. This post is primarily aimed at the total newbie, so if you are already familiar with DDDM and want to get serious about it at your organization, this post is likely not going to be very helpful.

Last thing I want to say is that while I plan to give examples of how specific products achieve their goals through DDDM, I have never worked for any of the companies I reference and cannot tell you for sure if they are following the practices I describe exactly. I am going to be purposefully broad about this in any case, so don't take my word as bond. This is really meant to be an introduction for the complete layman, which will necessarily involve a lot of hand waving.

With that preface out of the way, let's get into it.

## The Stone Ages

Let's start with a fairly innocuous question: how do big companies make their products better? If the CEO of Microsoft wanted 5% more people to use Outlook by the end of the year, how would they use their budget to do that?

If you were developing software in 2002, you might try: 
* Hire more people to make more features faster
* Hire smarter people to research human behavior and make a product people want
* Buy a competing company to acquire their userbase and intellectual property

These answers are all good, and for a long time they represented the primary ways to get ahead in software. If you weren't shipping fast enough, hire more hands. If people didn't like your products, hire experts to tell you why. And if someone did it better anyways, buy 'em out and call it a day.

This type of investment strategy is also conducive to the prevailing development paradigm of that era: "Waterfall"  development. I won't speak too much about different development strategies in this post, but here is a high-level view of how Waterfall works:

![Waterfall: design, build, test, ship]({{site.url}}/assets/posts/data-driven-design/waterfall_dev.svg)

In Waterfall development, software is produced in phases that cannot be started until the previous phase is complete:

1. First, requirements are collected and synthesized while the architecture and designs are decided. 
2. Then, engineers build the software based on the requirements.
3. Next, the quality team tests the code extensively, looking for bugs.
4. Last, the product is shipped out to the public. 

The team, after a wild release party, begins the process anew. 

When pursuing the investment strategies I outlined above, it's easy to see where the decisions fit into a waterfall model. You can beef up your implementation or test teams if you want to ship faster or higher quality products, or hire big shot product managers like me to design requirements if you want a product more people want. Simple!

So what's so bad about this approach? Well despite hiring a bunch of experts, you really can't draw any meaningful conclusions from the work they do. Ask yourself:

* How do you _really_ know those people you hired are working on the right stuff?
* How do you _really_ know those smart people you hired actually understand your customer and their needs?
* How do you _really_ know the IP you just bought from your competitor is the actual reason they were beating you?

While you can't make a product without people, and you can't succeed in an industry without subject matter experts, at the end of the day what you're participating in is _educated guesswork_. Your team could be on a truly disastrous trajectory and until your next major release comes out and you get your sales numbers back, there's almost no way to really know you've made a mistake.

## What is a team to do?

There's a fourth area to invest in here, beyond the three I outlined above. Companies have in the past decade started studying their customers and their behavior, adapting their software development processes to apply a more rigorous and scientific approach to implementing their designs. In [part two]({{ site.baseurl }}{% link _posts/software/2018-01-15-data-driven-product-management-part2.md %}) of this post, we will explore how data-driven decision management strategies can be introduced into the day-to-day process of software development, allowing a team to see insights into their customer base and retrieve feedback in real time without disrupting the overall experience for the customer.