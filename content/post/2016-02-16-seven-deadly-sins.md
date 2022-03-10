---
date: "2016-02-16T00:00:00Z"
title: 7 Deadly Sins of Open Source Software
---

There are plenty of things that you need to do right in order to properly maintain, publicize, and grow an open-source project. This is not that kind of post.

I'm writing about what you want to avoid at all costs. I don't mean mistakes, things that you might innocently wander into doing. Instead I'm talking about things you might do that feel wrong. It's because they are. And the knot you feel in your stomach when you look the other way? It feels worse on the receiving end.

Here are the 7 deadly sins:


#### Sloth

The first and perhaps most obvious is Sloth. You probably already know what I mean. A lazy repo-maintainer is an alienator, a frustration.

Sloth is bad because it turns away people who are ready and willing to help you out. It also turns away people who haven't decided if your library or tool is useful. If it already doesn't work with modern technology, they will slink away and search up another solution, or even roll their own.

When you are too lax in your basic duties, all you are doing is giving them plenty of time to think about how frustrating you are, about all the time they spent on their solution, and how it wasn't given an iota of your time.

_Virtuous patterns_:

* Answer that issue as soon as possible
* Give feedback on that pull request as soon as you can, even if it is to say "I see this; I can't get to it until time _x_."
* Release your changes frequently
* Put in the effort for a good CHANGELOG. It's going to take you about 2 minutes when you do a release for the lovagod.
* Upgrade your dependencies so your library works with the latest.

You can tell yourself, "I'm just lazy. I'll get to it." But to me? You are flat-out ignoring people, ideas, the software continuum. Log on, answer questions, fix up your code.


#### Gluttony

The opposite of ignoring pull requests is to accept absolutely all pull requests. We could live in a fantasy-land that every pull request has merit (especially when you are seeing pretty green checkmarks for that pull request). But the underbelly of a liberal acceptance policy is a repo that has lost its way. It then becomes a complicated, pointless mess.

_Virtuous pattern_: It’s ok to say no to pull requests that are counter to your vision for the project. Just explain why you’re saying “no” and, if possible, suggest an alternative project or solution. Saying no does not make you a Bad Person. But saying yes all the time? That does.

#### Pride

Being a sinfully proud repo owner means you think your repo is too perfect to touch. C'mon, man.

Committing this sin means several things:

  * Something about your project is so special ("easy," "powerful," "useful," ... ), that you think it doesn’t need to obey conventions, like having a README, styling, tests, or an issue log.
  * Lots of compatibility breakages.
  * Poor documentation. Here's a hint: saying "the documentation is in the code" doesn't help everyone. Maybe you have good docstrings. Hooray for you. You need to publish them.

_Virtuous pattern_: Be unafraid to question the choices you’ve made. Engage others when they have questions, because you're going to get some good ones. (And if you get the same question over and over, you need to figure out how to address that question before it comes to the repo.)

Always seek improvement with an open mind.

#### Wrath

Look, no matter how ugly that code is for the pull request, no matter if the person flatly ignored some of the rules you set out in your CONTRIBUTING file (because you have one of those!) or has wasted precious moments of your life with their dumb code and dumb questions...don't be a jerk about it.

_Virtuous pattern_: Constructive feedback.

#### Greed

* Stealing someone's commit or idea. Maybe that sounds awful to you, but trust me, I've seen it. If someone puts up code you need to completely refactor, you should do what you can to keep that person's commit in the logs.
* Worse: Stealing someone's commit or idea and putting it behind a paywall. I've seen this happen, too. Isn't that awful? Look, I know your project needs to make money at some point. But, a business plan that includes taking others' contributions and making customers pay for them has got to be the worst form of freeloading. It's like your buddy brings the chips to the party, then you charge everyone (including him!) for those chips, and keep the profits for yourself. Listen to what you're doing, man!

#### Lust

A.k.a. “this pull request looks great! Your code is great and your idea: great. I can tell you know what you're doing. Actually, could you also completely refactor an entirely different set of code that needs help? I’ll merge it after you do that.”

(My interpretation here, is that you are lusting after contributors and their skills.)

When a person is submitting a pull request, s/he wants to use the repo. In fact, they are probably dutifully getting it merged upstream, then they can pull the published library instead of dealing with a fork. That is awesome! Don't abuse your power by making them jump through hoops that are irrelevant to what they are trying to accomplish. If they are touching code you want refactored, then yes you can use this person's help. But be reasonable about it. If you want them to help you do a deeper refactor? Just ask him or her. But keep it out of this particular pull request. Otherwise you're begging this person to create a fork and avoid future upstream improvements. (Which the person probably has more of.)

_Virtuous pattern_: Understand the problem the person is trying to solve and help him/her get there. Don't stretch the scope of this person's work beyond accomplishing the original intent. If you need some help and this person is willing to do it, don't hold a PR hostage.

#### Envy

Envy in this context can mean a few different things.

  * Deliberately making it difficult for adopters to monetize your code
  * A ridiculous license agreement
  * No collaborators, just you
  * Shamelessly copy/pasting code or features from other projects (perhaps that's lust?)

Look, if your project is open source simply because you want that free Github repo, I'm not going to hold it against you. Just make that clear in your README. You're retaining some rights to this software. You can do that with a license, so pick the right one. (I'm just guessing, but if you're really that caught up about it, you probably are not posting it on the Internet, though.)

If you have a generous license and you're falling into some of the above bullet points? Then I call you out and say you really don't want your repo to be open source because you can't stand the thought of someone else 'owning' it.

  * _Virtuous pattern 1_: Add collaborators you trust, and cheer on other projects trying to accomplish a similar set of goals
  * _Virtuous pattern 2_: Have a fair license agreement

#### 8th Deadly Sin

This is mine: my blog doesn't have any discussion component, and therefore is lacking in transparency and a proper feedback loop. If you'll forgive me that, I'd love to hear what you think. Check the [about](/about) page and drop me a line if there are other things that drive you away from adopting or contributing to an open source project. I'd love to hear it.
