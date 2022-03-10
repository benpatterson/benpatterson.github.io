---
date: "2019-09-10T00:00:00Z"
description: One of my favorite times of year is October. There are almost too many
  reasons to count...
title: Hacktoberfesting well
---
One of my favorite times of year is October. There are almost too many reasons to count (my birthday, my twin brother's birthday, autumn, black heritage month, and on). [Hacktoberfest](https://hacktoberfest.digitalocean.com/) is without a doubt an annual highlight for me. To make it successful year-to-year, I've had to adapt.

At this point in my career, coding at work means picking up a neglected project, where I know I can take my time on it without falling behind, or without stepping on the toes of a team. Hacktoberfesting is also a great way to stay technically current and capable. It's also a place where I can see what folks are dreaming up, what problems they are confronting, and where there are gaps. It's nice to feel like one can lend a hand to keep them going. And seeing a pull request get merged? The giddiness never goes away for me.

It's become more popular every year, which is great for the community, but I must make adjustments on my end. As a person that can only dedicate certain segments of time, I've found myself jostled out of issue fixes by multiple folks who have more time available. I've seen PRs die due to infighting by maintainers. I've also seen development environments disappear (e.g., deciding to remove docker support in the middle of October). As such, I'm writing this post because I think there are some worthwhile tips to make hacktoberfest a good ride. Here are several things you can do to make it smoother.

#### 1. If you want to learn: make it at most 45% new. ####
I like to make it a learning experience while I'm at it. It's a great opportunity to pick up something new. The problem is, if it's completely foreign, it's going to be hours of research and ramp-up in order to make a pull request effective. But, coming in and saying "don't try anything new" is the kind of advice I would ignore. Once, I worked on a scala project as a way of getting familiar with the language. I picked a critical math library, and I dove deep, and it felt good. I found the commit that broke builds for them, and although I studied linear algebra in college, it proved to be too time-consuming to unwind the actual issue. Translating concepts that I long-ago grasped into a language that I was still learning, in tests that were not well documented.... Ultimately I never got my t-shirt that year, even though I'd made tremendous progress.

So, I like to make it at most *45% new*. Perhaps the language is familiar, perhaps the library is somewhat familiar, but maybe you're learning a new thing as part of it. It could be a new CI system, it could be a new kind of webservice, similar but different to ones you've worked in before. It could be a new language, but one a repo that is fairly uncomplicated. You'll come out of it a bit more knowledgeable, but you'll also be able to make an impact. 

#### 2. Don't get a repo that's too conflicted. ####
Some of the repos I really like working on are very popular, well-adopted, and well-supported. You've got the classic hits: your `requests`, your `activerecord`, your `moment`. Those foundational repos that folks know about in rando developer conversations. A couple years ago, I put in a pull request to a foundational framework. There had been a ticket sitting there for two hacktobers, and the ticket itself was written very prescriptively (removing a security hole in images on the default 404 page). The solution wasn't even in a new programming language; it was in an HTML template. So I went boldly forth and put in a pull request that matched the request. It felt like an incremental step forward. Then I watched the pull request fall into a debate amongst core contributors. Sometimes, incremental improvements are not wanted on mature repos. Instead the incremental work exposes much deeper issues, and that's what ends up being debated and sinking any progress. (I see this kind of pattern everywhere; not just open source repos.) Sometimes these repos likewise have enough cooks in the kitchen that viable pull requests are sidelined by internal debate. Don't get me wrong, I could have done better, too.  Even when submitting it, I was thinking, "this is what they wanted, so..."

Some repos are well-maintained and have mechanisms in place where foundational questions can be answered (or better, they are already answered in a CONTRIBUTING doc.) But for some repos there are hidden requirements or preferences at play, and pull requests can get sidelined. Even if a repo is popular, I avoid it unless I'm deeply familiar with it anyway. Fact is, the simple issues get addressed as a matter of normal development. 

If for some reason the popular repo is running squeaky-clean and there's little to no friction getting a pull request merged, I'd still be racing against other contributors who have more time on their hands. I've seen several efforts left permanently on a branch on my machine because someone came in and banged it out in a full day, when I was doing it on the side.

Overall I avoid the popular or mature repos (for Hacktoberfest) for those reasons.


#### 3. Don't get a repo that's too immature, either. ####
Another side to this equation is a repo that is so new or under-supportd that the `hacktoberfest` issues are super fundamental. For example, "add CI/CD" or "do performance tests". These are foundational things that the maintainers perhaps value, but not quite enough to invest in themselves. As far as pull requests go, they can sometimes be very chunky. Adding CI/CD for example, requires admin access if you're serious about getting it on the source repo. It is possible to set it up on a fork of course, but the act of getting it merged is much larger and requires coordination or even requesting a deeper level of access on this repo. My main concern with this approach is, again, if you want the minimum number of pull requests to qualify for your t-shirt, you're signing up for potentially a ton of effort for that one pull request.

#### 4. Choose nice maintainers ####
When I am close to choosing a repo or issue to work on, I like to look at past pull requests or open issues. Sometimes the maintainers are unhelpful or even jerks, particularly to people that are new to the repo. (Sometimes these are new programmers, and sometimes they are experienced programmers that just don't know the expectations of the maintainers.) Ideally, I will see a maintainer giving feedback to a pull request or issue. Are they respectful, no matter the contributor? Do they repeat themselves without getting irked? If there is code feedback, is it positive (even if it's direct)? There is an opposite problem as well: someone that notices you are comfortable fixing up things, and piles on requirements after you have a PR.

If you're thinking, "maintaining a repo is hard," I agree with you. I was the maintainer of a high-traffic Jenkins plugin a few years ago, and indeed I would see questions or pull requests that covered the entire range: sometimes a person saw an exception and didn't read it, but posted it and asked about it (oftentimes unrelated to the plugin), and there were also questions going into implementation details that I'd inherited where I didn't have a great answer, or even time to dig into how those decisions had been made. Maintaining an open source repo is hard, but if you truly value open source contributions, you need to value open source contributors and avoid the [7 deadly sins](https://www.fifteenlinesoffame.com/2016/02/16/seven-deadly-sins/).

#### 5. Make sure it's easy to test ####
Some repos ask for rigorous tests with a local test environment. That doesn't bother me at all. But if the repo is going to take hours of set up, then I may never get far enough to contribute. If there are unit tests already, simple setup for local development, or other easy levers to pull for validation, then I'm in for a good time. I personally feel strongly about verifying my changes, so I like to look at what that process is going to be like, from beginning to end.

#### 5+ If you worry about agreements, make sure you agree with them first ####
I've also been caught up with the legal agreements associated to contributing. One repo had a legal agreement associated with it. This is common and honestly it's usually a good sign of a well-run repo. However, in this particular case, the fine print was a bit harrowing for me. It included giving up rights to things I didn't even write for this particular repo, even things I'd written previously! I probably could've signed that agreement and nothing happened, but tbh I'd be losing a bit of sleep over it. If you're the kind of person that worries about these things, take a look at that early.

Ultimately there is a sweet spot for repos where you can fly in and make a meaningful contribution. This is the Goldilocks Continuum.

#### The Goldilocks Continuum ####
For someone with time constraints, the ideal target has repos and issues that don't get much traffic, but still get something. That means I'll be able to work on a nice, chewy issue for several days when I have free slots, but I'll have a good likelihood of feedback or even a merge without another hacktoberfester swooping in and knocking it out in a day. Alternatively, I need issues that are super easy and can get done in one sitting. So the Goldilocks Continuum for me looks something like this:
* Repos that gets hits, but not too many hits
* Maintainers that care about contributors
* Subject matter that is a little new to me, but not completely foreign
* Minimal set up, but not completely naked of development practices
* Issues that will take up the right amount of time

#### Good luck this October ####
It's a great time to contribute back to the community that has likely driven success for you, your learning, your company, and on. If you feel good about contributing open source software, then take some time in October, contribute, and get a free shirt. Everybody wins.

