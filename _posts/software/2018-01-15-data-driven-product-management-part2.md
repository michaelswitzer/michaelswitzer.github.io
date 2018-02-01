---
layout: post
title:  "Introduction to Data-driven Product Management: Part 2"
permalink: /software/:year/:month/:day/:title.html
type: Software
date:   2018-01-15
summary: The thrilling conclusion to part 1, wherein we explain Agile methodologies and how data-driven design strategies have changed the face of software forever.
---

## We're Back!
In [part 1]({{ site.baseurl }}{% link _posts/software/2018-01-01-data-driven-product-management-part1.md %}) of this post, we took on the mindset of a CEO looking to improve their companies' products through investing in more people, better people, and IP. In this post, we'll explore a fourth area of investment: _process_. We will describe how successful companies have upended their development strategies and implemented processes that allowed them to get better insights into their customer base through a technique called "data-driven decision making strategies" (DDDM). We'll conclude with an example of how Amazon continues to grow traffic on their front page without seriously risking a misstep and interrupting their revenue streams. Let's get started!

## What happened to my versions?
Back in the stone ages, when you bought software like MS Word or TurboTax it had a version attached to it. Your copy of Photoshop 6 had major feature improvements over Photoshop 5, and they were released about a year apart. You may have noticed that most products don't do this anymore, and web-based products like the Amazon homepage and Google search don't even show you a version number. What gives? This change reflects a major shift in software design practices toward a method known as "Agile development". What is Agile in a nutshell? Well let's start with the method we explored in part 1, known as Waterfall.

![Waterfall: design, build, test, ship]({{site.url}}/assets/posts/data-driven-design/waterfall_dev_photoshop.svg)

In Waterfall, each version of your software is divided into three major parts: design, build and test. At the end of this cycle, usually months later, you release a full fledged version update with big shifts from version to version. This method worked well for a long time, and made sense in a world where shipping software couldn't be done easily over the internet. Selling software in a physical store required supply chains to be set up, CDs to be stamped, etc., and you usually had a long lead time to work the kinks out. You could align your Waterfall-based releases with the physical release of software and make a successful product out of it.

After the internet became widely available, this methodology made a lot less sense and companies that released faster and faster became more and more successful. As a quick example, if google.com only updated their search engine index and algorithm once per year, they obviously wouldn't be in business. So companies completely changed their outlook, moving to a methodology where design, build and test are fully integrated into a consistent pipeline:

![following Agile: design, build and test is done on separate branches and merged to master later]({{site.url}}/assets/posts/data-driven-design/agile_dev.svg)

The master branch of the product is considered to be release-quality at all times, because all of the experimental work is performed and tested on separate branches of code. Once the branch is merged, integration tests are run to ensure that quality is maintained throughout.

Using agile methodologies, the idea of a major release was no longer necessary. Code was shipped very often, in much smaller chunks (usually one feature at a time) and could be given to the customer at the rate the developers churned it out with very little overhead. This enabled web-based apps to ship code quicker and more often, and really changed the face of software development forever.

A quick aside for a disclaimer: This process explanation is just scratching the surface of how these systems work. There are many many books written on development practices and I am dramatically simplifying things for the sake of getting to the data stuff (I promise it's coming!). 

So Waterfall to Agile was the first huge shift. What was the next one? I think you can guess, but if you're truly doubting that I'm finally getting to the point, the answer is DDDM.

## Let's get serious
When dealing with a highly available software product such as an e-commerce store or a search engine, the stakes are very high. Tiny preterbations in how things work can have massive effects. I heard an anecdote from a PM on a major ecommerce product that one of their developers checked in a change that moved their checkout button one pixel down, and it caused their revenue to plummet by 6%. Six percent for one pixel! In a growth oriented software economy, this could be a death sentence for a product. Why did one pixel mean so much? After spending a lot of money on researchers to figure this out, it turned out the checkout button had been moved outside of the [Z-shaped scan pattern](https://uxplanet.org/z-shaped-pattern-for-reading-web-content-ce1135f92f1c) that eyes usually follow when reading a web page.

I mentioned that a 6% drop in revenue could spell death for a product. So why did this one survive? And how did they correct the problem before it was too late? It turns out the company was at no risk at all, thanks to the DDDM practices they had implemented. The vast majority of their customers had never even seen the change that caused such devastation to their bottom line and the research the company had paid for to figure out the root cause was not so that fingers could be pointed at a developer for messing up, but to improve future development on the product.

Here's how they did it:

![Agile, but with an experiment every time you merge to master branch]({{site.url}}/assets/posts/data-driven-design/agile_dev_DDDM.svg)

At the end of the Agile pipeline, instead of shipping their code out to all of their customers, they only show a select few their new feature. Automated processes will ship their code to a tiny fraction of users, then start tracking the user's behavior automatically. User performance can be measured through Key Performance Indicators (KPIs), which can mean revenue, user retention rate, CPU overhead, or any other priority of the company or department. I'll write a post on selecting KPIs in the future, but for now let's work with revenue.

Upon pushing the new code to the ecommerce site, about 0.001% of users browsing to the site saw the checkout button moved one pixel. The automated build process tracked the revenue of users that were browsing the new site vs. the old site, and produced a report indicating that the revenue had dramatically dropped with the new version. With zero human intervention, the build process detected this and reverted the change, saving the company millions. The team responsible for the change was informed and it was back to the drawing board for them.


## A Real World Example
So you don't have to rely on my 6% anecdote:

![the Amazon home page]({{site.url}}/assets/posts/data-driven-design/amazon-home-page.png)

The Amazon homepage has hundreds of clickable elements and updates every single day with new products and feature announcements. It also drives a massive amount of revenue for the company. If the site went down for even a few minutes, it means [millions](https://www.digitalcommerce360.com/2016/03/11/how-much-did-amazons-outage-cost-online-giant/) of dollars lost. You would imagine it is very frightening to work on a team that manages the front page. But the vast majority of the risk involved is mitigated through their build process. Let's say the team is directed to increase checkout button clickthrough rate for the page, and they have a few different proposals for how:

* Program Manager A wants the checkout button to be 10% bigger.

![the Amazon home page, with a bigger checkout button]({{site.url}}/assets/posts/data-driven-design/amazon-home-page-A.png)

* Program Manager B wants the ad on the page reworded to something more persuasive.

![the Amazon home page, with a more pursuasive ad.]({{site.url}}/assets/posts/data-driven-design/amazon-home-page-B.png)

* Program Manager C wants the page to automatically redirect to the checkout screen after five seconds if the user doesn't do anything.

![the Amazon home page, with automatic redirects.]({{site.url}}/assets/posts/data-driven-design/amazon-home-page-C.gif)

In the past, they might appeal their proposals to their director of product management, and try to make their cases with good old fashioned powerpoint. Now they just get to work implementing all three changes and let them all duke it out in a no holds barred cage match.

Three separate experiments are run by the build process and the results come rolling in:


<table>
  <tr>
    <th></th>
    <th>Experiment A</th>
    <th>Experiment B</th>
    <th>Experiment C</th>
  </tr>
  <tr>
    <th>Revenue</th>
    <td>+1%</td>
    <td>+1%</td>
    <td>-46%</td>
  </tr>
  <tr>
    <th>Clickthrough Rate</th>
    <td>+2%</td>
    <td>+3%</td>
    <td>+54%</td>
  </tr>
  <tr>
    <th>Satisfaction Survey</th>
    <td>0</td>
    <td>+1%</td>
    <td>-64%</td>
  </tr>
  <tr>
    <th>User Retention Rate</th>
    <td>+1%</td>
    <td>+2%</td>
    <td>-92%</td>
  </tr>
</table>


A and B results provide incremental improvements to the clickthrough rate, so those PMs are pretty happy. PM C, though, is beside themselves and cannot stop bragging to everyone. They boast a massive improvement to the metric their boss asked them to improve! Surely a raise is in sight for them!

But PM C's change never makes it to production, because it made all the other KPIs much worse. They've decided to force their users to go to the checkout screen, and didn't reckon on the consequences catching up to them. Done right, DDDM is very hard to cheat. There are no short cuts to beat the system with.

A and B's features make it to production and they enjoy a healthy bonus the following year.

## Conclusions

Does DDDM have any downsides? Sure. It can be expensive to implement these complex testing frameworks and systems, so smaller firms have difficulty keeping up with larger companies. It also, for better or for worse, removes some of the human element of product design. If developers are left unsupervised and the KPIs are prioritized poorly, [dark patterns](https://youtu.be/e8r47hZX2G8) of software design can emerge. Even in more ethically produced products, users can begin to feel alienated or manipulated if they catch on to the game that the companies are playing with them. These arguments are worth exploring, but since DDDM is here to stay until the next big paradigm shift inevitably comes, we are better off just trying to make it as functional and powerful a tool as possible.

The freedom to try new things with zero risk has been revolutionary for software. Incremental improvements are now happening constantly to nearly every major web-based product, while you are experimented on without even knowing what is happening. And now when developers or PMs face a fork in the road or a question of how to implement a new feature, it is often the case that _both_ features will be implemented and tested, leaving the strongest implementation to show beyond any shadow of a doubt that it is superior.

There are huge implications for scaling and growing the company as well. While hiring great employees still makes a huge difference, firms can distribute good leaders more thinly across the organization, enabling larger teams to contribute on the same products and still maintain a cohesive vision and strategy. Teams can gain significantly more autonomy now that their decisions are validated by data rather than the intuitions of leadership. A bottom-up culture has grown among tech and now most major feature decisions are made at a lower level of management. Management's role has also evolved, requiring shrewd data analysts rather than business people with good instincts. Rather than issuing directives like "build me this feature", they can delegate tasks like "increase checkout button clickthrough rate by 6% in the next year" and allow teams the ability to figure out what that means. DDDM has created an entirely new world for software development.

## Thank you
Thank you for reading this post! It was fun to write and I hope you learned something along the way. Though you might not use DDDM directly in your career, understanding how software is made can help you understand how to be a better consumer. If you are making software today and do not employ DDDM, I highly recommend reading more and pitching some ideas to your employer. If they won't listen, they may not be around in the future to hear you out.

For continued reading I recommend the following resources:

* [Coursera course on DDDM](https://www.coursera.org/learn/decision-making)
* [Martin Fowler's work on Continuous Integration](https://www.martinfowler.com/articles/continuousIntegration.html)
* A good statistics or econometrics textbook. I used [Andrew Gelman's Bayesian Data Analysis](https://www.amazon.com/gp/product/1439840954/) book back in college though I can't speak for others. For true nerds, [his blog](http://andrewgelman.com/) is excellent.