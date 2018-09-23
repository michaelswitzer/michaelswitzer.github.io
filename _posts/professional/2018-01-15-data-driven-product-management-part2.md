---
layout: post
title:  "Data-driven Product Management Part 2"
permalink: /professional/:year/:month/:day/:title.html
type: Professional
date:   2018-01-15
summary: Follow up to part 1. We explain at a high level how adopting Agile methodologies have changed software design, and describe how data-driven design strategies (DDDM) is applied to deliver quality software with minimum risk to revenue interruption.
---

### We're Back!
In [part 1]({{ site.baseurl }}{% link _posts/professional/2018-01-01-data-driven-product-management-part1.md %}) of this series, we explored the three most straightforward strategies companies use to make software better: Hiring more people, hiring more effective people, and acquiring IP. 

In this post, we'll explore a fourth area of investment that has revolutionized software development in the last decade: _improving development process_. We will describe how successful companies have radically changed their development strategies through Data-driven Decision Making (DDDM).

We'll conclude with a (fictional) example of how companies like Amazon ship features on their highly available websites without risking a major breakdown or revenue interruption.

### Software before the internet
Before the internet became widely available, software was bought in a store instead of downloaded. Since it was relatively expensive to print CDs and floppy disks, companies couldn't distribute their software very often, and so they planned their product releases on a fixed cycle. Since their release dates were set ahead of time, it required a lot of up-front planning to figure out what they were going to be able to finish by the time the next release came around.

In [part 1]({{ site.baseurl }}{% link _posts/professional/2018-01-01-data-driven-product-management-part1.md %}) we looked at the Waterfall method of product development:

![Waterfall: design, build, test, ship]({{site.url}}/assets/posts/data-driven-design/waterfall_dev.svg)

This design paradigm involves significant upfront planning and estimation, so it seems natural that this would be the primary way to make software when you could only distribute it once in a while.

After internet speeds improved and it became easier to get updates online, though, Waterfall development started to feel handicapped due to its low cadence and inconsistent product quality. It wasn't particularly efficient to plan extensively up front for all possible outcomes, and if something unexpected is discovered in the final test phase it could throw the whole release. So teams started looking for ways to release faster and smaller, to reduce risk of going too far off the rails before it was too late. 

### Enter Agile
The biggest paradigm that emerged from this process of reinvention was called Agile development. In Agile, design/build/test are done on separate branches at the feature level instead of the release level, and the master branch is consistently maintained at releaseable quality:

![following Agile: design, build and test is done on separate branches and merged to master later]({{site.url}}/assets/posts/data-driven-design/agile_dev.svg)

The master branch of the product is considered to be release-quality at all times, because all of the experimental work is performed and tested on separate branches of code. Once the branch is merged, integration tests are run to ensure that quality is maintained throughout.

Using Agile methodologies, the idea of a major release was no longer necessary. Code was shipped very often and in much smaller chunks, and could be given to the customer at a higher cadence.

This did not completely remove uncertainty, though. Any time code was shipped, it could still wreak havoc on the business if it was unpopular or made the user experience worse. Teams needed a way to measure their improvements objectively, rather than based on intuition.

### Scientific method to the rescue!
Teams decided to start treating their features like experiments. If they showed the work to just a few of their users and collected data based on their behavior, they could get a good sense of whether the feature was a good thing or not.

To explain this a little bit better I'll go through a fictional example of what it would be like to manage Amazon's home page. I do not work for Amazon and thus cannot tell you anything about the exact methodologies they use to implement DDDM, but rather the general process used to assist in decisionmaking. Let's get started!

### What's at stake

![the Amazon home page]({{site.url}}/assets/posts/data-driven-design/amazon-home-page.png)

The Amazon homepage has hundreds of clickable elements and updates every single day with new products and feature announcements. It also drives a massive amount of revenue for the company. If the site went down for even a few minutes, it means [millions](https://www.digitalcommerce360.com/2016/03/11/how-much-did-amazons-outage-cost-online-giant/) of dollars lost. 

Despite this, Amazon grows its traffic on this page consistently. How does it maintain its growth rate without any missteps accidentally causing their performance to tank unexpectedly?

Let's say the team is directed to increase checkout button clickthrough rate for the page, and they have a few different proposals for how they might go about this.

* Program Manager A wants the checkout button to be 10% bigger.

![the Amazon home page, with a bigger checkout button]({{site.url}}/assets/posts/data-driven-design/amazon-home-page-A.png)

* Program Manager B wants the ad on the page reworded to something more persuasive.

![the Amazon home page, with a more pursuasive ad.]({{site.url}}/assets/posts/data-driven-design/amazon-home-page-B.png)

* Program Manager C wants the page to automatically redirect to the checkout screen after five seconds if the user doesn't do anything.

![the Amazon home page, with automatic redirects.]({{site.url}}/assets/posts/data-driven-design/amazon-home-page-C.gif)

In the past, they might have resolved these priorities by submitting proposals to their director of product management, who would evaluate whether the features might be beneficial to the business. At companies like Amazon, though, this answer is found primarily through data analysis. By applying DDDM, they release experimental versions of each feature and determine their objective value to the company, with a fully automated process for determining success:

![Agile, but with an experiment every time you merge to master branch]({{site.url}}/assets/posts/data-driven-design/agile_dev_DDDM.svg)

Following this model, all three teams work to release their respective features. Whenever they happen to finish their work, they check the code into an experimental branch, where a very small fraction of the users of the site sees their new feature. An automated system then evaluates how those users react to the changes. If the experimental run succeeds in improving the product, the code is uploaded to the main branch where the rest of the users can use the new feature.

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

Many companies do not see the immediate value in applying DDDM to their development process. It can be expensive to implement these complex testing frameworks and systems, and it means a significant amount of development cycles are not spent on revenue generating activities. If DDDM is implemented poorly, the emergence of [dark patterns](https://darkpatterns.org) can cause a decline in userbase over time due to growing mistrust of the product. 

Despite this, DDDM has become the most important force driving modern software development. The freedom to try new things with virtually zero risk has been revolutionary for software. Now when developers or PMs face a fork in the road or a question of how to implement a new feature, it is often the case that _both_ features will be implemented and tested, leaving the strongest implementation to show beyond any shadow of a doubt that it is superior.

Implementing DDDM has major implications for scaling and growing companies as well. Deferring significant amounts of decisionmaking to data analytics allowed companies to hire less managers and more engineers. Since team performance is measured objectively, companies can effectively scale without having to find visionary leaders for each vertical they get involved in. Teams can gain significantly more autonomy and a consistent atmosphere of open experimentation and innovation emerges.

The role of management has also evolved, requiring shrewd data analysts rather than business people with good instincts. Rather than issuing directives like "build me this feature", they can focus on KPI optimization and prioritizing the areas of their business that maximize growth and revenue.
 
The process of software development has evolved over time as much as software technology. After Agile development replaced Waterfall, DDDM applied a scientific approach to shipping code and changed the face of software forever.

## Thank you
Thank you for reading this post! It was fun to write and I hope you learned something along the way. Though you might not use DDDM directly in your career, understanding how software is made can help you understand how to be a better consumer. If you are making software today and do not employ DDDM, I highly recommend reading more and pitching some ideas to your employer. If they won't listen, they may not be around in the future to hear you out.

For continued reading I recommend the following resources:

* [Coursera course on DDDM](https://www.coursera.org/learn/decision-making)
* [Martin Fowler's work on Continuous Integration](https://www.martinfowler.com/articles/continuousIntegration.html)
* A good statistics or econometrics textbook. I used [Andrew Gelman's Bayesian Data Analysis](https://www.amazon.com/gp/product/1439840954/) book back in college though I can't speak for others. For true nerds, [his blog](http://andrewgelman.com/) is excellent.