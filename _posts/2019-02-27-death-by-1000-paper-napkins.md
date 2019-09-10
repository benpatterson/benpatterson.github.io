---
layout: post
title: Death by 1,000 Paper Napkins
description: Today I reflect on the problem where we put too many nice things into a product and it kills the product.
image: "{{ site.baseurl }}/assets/images/orange-napkins.jpg"
---

The popular phrase "Death by 1,000 Paper Cuts" usually refers to a problem that kills a company, team, or product because there are too many little problems adding up. Today, I reflect on the opposite problem: too many nice things. Let's call it Death by 1,000 Paper Napkins.

It's a Malthusian nightmare of features or functionality. The app, the users, or the products die because their space is so crowded, they cannot nourish themselves.

In my experience, I've seen this occur in a few different ways:

1. Noise
1. Feature bloat
1. Complexity

![stack of napkins]({{site.github.url}}/assets/images/orange-napkins.jpg){: .center-image }

### Noise
The classic example of noise is too many pop-ups. Most of what we see today are the different ways a website can claim to help you. There are interruptions to introduce you to chatbots, there are help pointers and there are intro modals. In isolation, each of those can be useful and helpful, but adding them all together turns into a wall of noise. The website becomes unusable. From the perspective of accessibility, it truly can become unusable, if keyboard interaction does not allow a user to close a modal, toast, etc. This might sound like an exaggeration, but I've seen it without even trying. Noise like this rarely starts as a sudden blast of sound; it slowly rises from a murmur, and this is where there is risk.

This kind of problem plagued websites and applications in the late 1990s and inspired a host of desktop applications and browser plugins that still exist today. If we are too abusive of toast notifications and the like, we will see a similar cottage industry arise. In the near-term, you might simply be driving users away from your application to a quiet competitor.

### Bloat
Another form of noise comes from a good thing: capabilities. We get many capabilities with minimal effort if we pull in 3rd-party applications to do the work for us. It's a completely sensible development or business decision: buy vs build. Without a holistic view however, it adds up. I previously worked for a company that used a total of four different analytics tools to gather user information. Those tools were used by different departments, but it resulted in heavy pages for end-users. Even when reducing sync transactions the overall transaction load on browsers was heavy, and the page weight itself was heavy, too. Many analytics tools do not want you to cache their tooling either, which means end users are carrying that weight around as they navigate.

Another manifestation of this overload is in product features. When user experience drifts from simple to complex, it does not happen suddenly with one feature. Rather, it slowly adds up over time. UX thinkers among us have attempted to make this measurable (interesting posts [here](https://www.usability.gov/how-to-and-tools/methods/system-usability-scale.html) or [here](https://uxdesign.cc/measuring-and-quantifying-user-experience-8f555f07363d) ), with things like surveys, number of clicks needed to accomplish tasks, and other metrics. Having many features isn't necessarily a problem on its own, but if user experience is not a highly held value across teams, you may have a dedicated cadre of power users and little else. 

### Complexity
In the ebb & flow timeline of frameworks across the industry, some become more powerful and more complex, leaving openings for "new, simple `<insert framework type here>`". You not only see this on products and websites; you see this on frameworks. It is not always a problem, but it can add up to one.

A great example of this is in the configuration settings. This could be for a user, an application, or a framework. How many configuration points do you have for running your application? How about your users? How far back does backwards-compatibility go? When using all of the default settings, how easy is it to spin up your product? These are applicable questions when thinking about configuration sprawl. The larger the sprawl, the more expensive changes become due to testing, risk, and so on. Of course, sometimes sprawl is ok. The more widgets you have to adjust, the more powerful the system becomes. It's the unfettered expansion that can result in suffocation.

Complexity and sprawl is another important area to measure; and it's not a matter of counting configuration duckets. Indeed, complexity can be measured when thinking about things like cyclomatic compexity. But value -- particularly for configuration items or backwards compatibility -- can be approximated when measuring usage. When building an application that is installed onsite, for example, this is often a step that is overlooked and costly down the line. If there is some level of phoning home or other (safe, reasonable) approaches to providing telemetry on how your product or framework is used, then it can become much easier to accurately foretell which napkins are disposable.

### 1,000 Paper Napkins
Similar to 1,000 paper cuts, death by 1,000 paper napkins can only be avoided by keeping that count under 1,000. It's a healthy dose of discipline along with prioritization and, potentially, drawing some lines you refuse to cross.

