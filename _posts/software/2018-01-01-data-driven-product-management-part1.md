---
layout: post
title:  "Introduction to Data-driven Product Management: Part 1"
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

This type of investment strategy is also conducive to the prevailing development paradigm of that era: "Waterfall"  development. I won't speak too much about different development strategies in this post (that's for another day) but it is important to point out here that every aspect of software development in inextricably linked together: Investment strategies lead to hiring strategies lead to development strategies lead to shipping strategies, and changing one development paradigm can often impact the entire process.

![Waterfall: design, build, test, ship]({{site.url}}/assets/posts/data-driven-design/waterfall_dev.svg)

In "waterfall" development, software is made in distinct drawn out phases that cannot be started until the previous phase is complete. 

These phases are:

1. Requirements are collected and synthesized. 

2. Software is designed and built.

3. A separate team ensures it has the quality necessary to ship.

4. The product is shipped out to the public by a separate business unit. 

The team, exhausted from their release party, begin the process anew. 

When pursuing the investment strategies I outlined above, it's easy to see where the decisions fit in a waterfall model. You can beef up your implementation or test teams if you want to ship faster or higher quality products, or hire big shot product managers to design requirements if you want a product more people want. Simple!

So what's so bad about this approach? How has software development changed since then? Why is this section titled "The Stone Ages"?

The answer lies in the _source_ of your knowledge. Try and answer these questions:

* How do you know those people you hired are working on the right stuff?
* How do you know those smart people you hired actually understand your customer and their needs?
* How do you know the IP you just bought from your competitor is the actual reason they were beating you?

While you can't make a product without people, and you can't succeed in an industry without subject matter experts, at the end of the day what you're participating in is _educated guesswork_. Your team could be on a truly disastrous trajectory and until your next major release comes out and you get your sales numbers back, there's almost no way to really know you've made a mistake.

## What is a team to do?

There's a fourth area to invest in here, beyond the three I outlined above. What if instead of asking your employees what the customer wants, you figured out how to make the customer tell you directly? Seems simple enough, and it even fits into your current paradigms! Just get those experts you hired to run some focus groups and user surveys and let the customer speak for themselves. Sounds simple enough, right? Well while those methods can get some useful information, they are pretty expensive to do all the time and can disrupt the flow of development by introducing delays or just producing ambiguous or bad data. In order for this approach to be useful, it needs to be _baked into the process_. And to do that, it takes a total reinvention of how software is made.

We've now identified the problem, and the direction we want to move in for the solution. There is a long way to go! In [part two]({{ site.baseurl }}{% link _posts/software/2018-01-15-data-driven-product-management-part2.md %}) of this post, we will explore how data-driven decision management strategies can be introduced into the day-to-day process of software development, allowing a team to see insights into their customer base and retrieve feedback in real time, without disrupting the overall experience for the customer.

Thanks for reading the first post on my professional blog. Expect more to come.

Update: [Click here to read part 2 of this series.]({{ site.baseurl }}{% link _posts/software/2018-01-15-data-driven-product-management-part2.md %})