---
layout: post
title: Don't Adjust Your Behavior; Adjust Your Environment
---

Would you board a plane in order to travel 10 miles?

What if traveling those ten miles looked like this? [^1]

![grand canyon]({{site.github.url}}/assets/images/grand_canyon.jpg){: .center-image }

Sometimes it takes a magnitude more energy to cross what is otherwise an easy stretch. This could be finding out why the engine light is on; it could be mopping the floor; it could be running tests.

To a certain extent, I'm talking about cost that's difficult to quantify. You are a smart person, you should trust your gut. If you're doing _x_ over and over again, you don't like it, and find you're compromising for otherwise-unhealthy behavior, then something's wrong. Not with you: with _x_.

I once worked for a company that had better coverage numbers for the acceptance tests than it did for the unit tests. Arguably, that's fine. Your code is covered. Maybe even with acceptance tests, it's covered "better". However, it is costly and time-consuming. Running 10 acceptance tests might take a couple of minutes; whereas running 10 unit tests could be done in under 1 second. Now blow that out to 800 tests and you are wasting precious time.

But _why_ was coverage so much better? I could blame, in part, poor choices, poor culture, etc. However, one reason is that they were simply **easier to write** than unit tests. Useful unit test base classes were non-existent. Repeatable patterns were not around, either. Crucial setup steps for things the application did, even having an available mocking library---all missing. (Whereas, these kinds of things existed in the acceptance test framework).

The only thing that these gaps did was promote bad behavior, and that behavior went unchecked. Not because the department was flooded with bad people, but because **we were not concentrating on the behavior itself**.

*Given*

* I am a conscientious developer. I want to test my code.
* I have a deadline I'm contending with.

It's a simple, common scenario. The question is, what's the best pathway to answering those two things? Automated tests! Hurray. But _which_ automated tests will be used?

Answer:

* Sometimes, it's the one that's the fastest to write, even if it's the slowest to run.

Once we observe the counter-intuitive decisions we commonly make, and step back to look at the overall landscape, we can understand that the landscape itself needs to change.

[^1]: Photo copyright 2010 by National Park Service, available via creative commons. Original [here](https://www.flickr.com/photos/grand_canyon_nps/5476589113)

