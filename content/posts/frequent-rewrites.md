---
title: "Frequent Rewrites"
date: 2019-02-02T14:11:20Z
draft: true
---

Around a month ago, a 2017 paper on [software engineering
at Google](https://arxiv.org/pdf/1702.01715.pdf) showed up on [Hacker News](https://news.ycombinator.com/item?id=18818412).

The first comment chain in the thread was on Section 2.11 in the paper where Fergus Henderson,
the author states the following:

> Most software at Google gets rewritten every few years.

Many commenters found this to be wasteful, citing the Gmail redesign as an example failure due
to this practice. Others noted that the alternative of bolting on bug fixes to existing code isn't much better.

I found it pretty interesting and since I'm a student with absolutely zero experience maintaining software for more than a couple months, today I'm going to explain to you everything you should know about this topic.

![](https://cheeseburgersnmore.com/images/kidthumbsup3.png?crc=3927708029)
_Trust me. I definitely know what I'm talking about._

__If youYou're probably going to rewrite much of your code in a few years anyway.__

## The Tragic Rewrite Process
1. Product gets built and then released.
2. Product is maintained but technical debt builds up as people leave.
3. The existing code becomes difficult to maintain, developers start pushing for
a rewrite.

## The Incremental Rewrite Process