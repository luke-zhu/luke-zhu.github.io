---
title: "A Better Software Testing Curriculum"
date: 2019-02-15T10:55:35Z
draft: false
---

I'm currently taking a class on software testing while abroad and
one thing that's really bothering me is the irrelevance of the material.
In the first lecture, the professor talked about how testing mainly exists
to improve software quality, which makes a lot of sense. However, the lectures
since have been on things like how to divide the input space of a function into categories and calculating different code coverage metrics.

In my intro CS courses, I learned about unit tests, edge cases, and white-box vs. black-box testing.
In this course, I'm learning about the theory behind creating perfectly-tested programs.
However, the most fundamental questions I've had
when writing my own test cases are barely even covered:

- How many tests should I write?
- What should I even test?
- Is the test I wrote good?
- How should I include a database or flat file in my test?
    - Should I even do this?
- Why are my tests so useless?
- What is the point of writing test cases?

At this point, I end up reading an article on testing at least once a week.
The worst part is that much of the advice given is some form of
keep reading/writing test cases until you get better.

Is that really the best we can do? In every one of my computer systems courses
(networks, distributed, databases), there is a huge emphasis on _tradeoffs_ and
understanding the underlying details which cause those tradeoffs. Given that
most people seem to decide between software testing techniques by analyzing the tradeoffs,
wouldn't it make to use a similar approach, especially since this tradeoff-oriented teaching approach seems to be working?

There are tons of engineers without
an advanced degree working on cloud platforms, containers, and SDNs.
For my networks class last fall, I (along with many other students) was able to understand the TCP RFC and implement
a TCP/IP stack from scratch. At the same time, the only useful test case I wrote for
my program was this terrible python script which checked that I could transmit
'hello' from one node to the other.

Maybe we could see a similarly big impact on software engineering if it became standard for students
to know all of the common testing techniques, their tradeoffs, and how to implement them.

## A Draft Curriculum

The curriculum could be similar to that of a computer
security course, which generally covers networks, cryptography, and
 the web.

### Topics
- Defining the goals of testing
- Defining software quality
- Different testing techniques in-detail
    - Unit, integration, end-to-end tests
    - UI and user testing
    - Load and performance testing
    - Continuous integration
    - Mocks, BDD, TDD, regression tests
- Common testing design problems
    - [Common types of bugs]( (http://landing.google.com/sre/workbook/chapters/postmortem-analysis/))
    - Production and dev environment differences
- Non-testing techniques
    - Logging, monitoring, static analysis, comments, data validation, assertions

### Project Ideas
- Testing a graph algorithm implementation
- Testing a 3-tier web application
    - Handling different environment variables
    - Handling differences between development and production environments
- Testing a system/platform like a simple operating system, database, or DNS service
- Building a UI testing framework

### Homework Quesiton Ideas

__# 1: Computer Security:__ When is it more appropriate to use a GET request, and when is it more appropriate to use a POST
request?

__Software Testing:__  When is it more appropriate to use a unit test, and when is it more appropriate to use an integration test
request?

__#2: Computer Network:__ Why can’t A and B, both being behind NATs, talk to each other by default? _(a NAT spec is given beforehand)_

__Software Testing:__ Why can’t A and B, both being in different directories, be tested at the same time by default? _(we can give a description of the build spec)_

__#3: Databases:__ List the ACID properties. Explain the usefulness of each.

__Software Testing:__ List 5 software quality characteristics. Explain the usefulness of each. _(OK this isn't great..)_

## Some Topics In-Detail

#### Defining Software Quality: ISO-9126
The most well-known software quality model is probably [ISO-9126](http://www.sqa.net/iso9126.html),
which identifies 6 main characteristics of software quality:

- Functionality
- Reliability
- Usability
- Efficiency
- Maintainability
- Portability

I've personally found it useful to keep these in mind when reviewing my own code.

#### Software Quality: SLOs
It's fairly difficult understanding how to balance velocity and quality.
I think [Service Level Objectives](https://landing.google.com/sre/sre-book/chapters/service-level-objectives/) are
a good way to help determine the desired level of software quality.

### Non-Testing Techniques

There are other techniques that also affect software quality outside of testing.

- Source code:
    - Assertions
    - Validation methods (for data and configuration)
    - Error handling code (`try: ... except: ...` in Python)
    - Type annotations (if needed)
    - Comments
    - Documentation
    - Good variable/method names
- Using a static code analyzer (or an IDE)
- VCS:
    - Commit messages
    - Pull request checklists
- Logging
    - Structured Logging (like [`logrus.JSONFormatter`](https://godoc.org/github.com/sirupsen/logrus#JSONFormatter))
    - Contextual Logging (like [`log4j.ThreadContext`](https://logging.apache.org/log4j/2.x/manual/thread-context.html))
- Monitoring
- Tracing
- Manual testing