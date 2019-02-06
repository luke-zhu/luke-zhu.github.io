---
title: "Coding More Quickly"
date: 2019-02-06T19:28:27Z
draft: false
---

- Write test cases.
- Identify cognitive load, then simplify the problem.
- Identify the quality level your code should reach.
- Do things more carefully.
- Get used to your tools
- Don't learn new things.

Some ways to code more quickly:

### Write a test case to verify that your code works.

_Why:_ If you're like me, you celebrate when your code work on the first try. If your code is marginally complicated, It's [less costly](http://blog.celerity.com/the-true-cost-of-a-software-bug) 
     to make sure your code works before it's in production. 

### Reduce your problem into smaller chunks.
_Why:_ Your brain is very small. Trying to keep everything in your brain is like trying to store critical data only in the cache.

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/0c/ComputerMemoryHierarchy.svg/1920px-ComputerMemoryHierarchy.svg.png" style="max-width:80%;max-height:400px">

A rule of thumb I use is that I stop to chunk down tasks if I'm starting to feel the affects of cognitive overload.
  
If you are feeling some of the below symptoms, you should try taking a break.

- You decide to write a TODO or update some documentation and then you can't remember what you need to do.
- You notice yourself just staring into space thinking very hard about ... something?
- You are making a lot of typos.
- You are randomly scrolling through the file.
- You have a strong urge to not write tests or documentation.

Now I don't have scientific evidence that reducing cognitive load increases productivity, but here
are some strategies you can use

- Iteration - Write prototype (pseudo)code and then cycling through a few times to turn that into production-grade code.
- Layering/checkpointing - Split the task into different steps. Complete each task and verify that your code is correct at that stage.

Another way to think of things is to turn your task into a tree (or graph) of easier sub-tasks.

### Know how reliability your code needs to be

_Why:_ We have a tendency to either aim for perfection or to just get shit done quickly.

After you have that number, it becomes a lot easier to decide in the moment whether you should
rewrite or just quarantine that terrible piece of code.

### Get used to your tools (and don't switch all of the time)

_Why_: It takes time to get familiar with a new IDE, cloud provider, and/or programming language.
If your goal is to write code quickly, then you will not want small kinks about your text editor
or operating system distracting you.

Don't play around with the base tools that you use _unless you are willing
to take the short-term loss._

- Operating system
- Web Browser
- Programming Language
- IDE/Editor
    - Keymap
- Cloud Service Provider

At the same time, it pays off the reflect and think about what tools you use
often use. You might notice that you are using

### Do Things More Slowly

_Why_: If you are making typos, losing track of the task, or not taking care
   of unhandled conditional states _and you know that you shouldn't be making those slips_, then
   you can just slow down and avoid them. As I said before, the brain is small.

### Don't Learn New Things

_Why_: Seriously. If you just care about coding quickly, then use the things you are familiar with.
    Even if you only used a tool over a weekend, you'll probably end up saving 5-10+ work hours just
    from having that experience.
    
## Also: Everything has a tradeoff
To be honest, I've just been rambling for a while, but as you get more experience, you will
understand that nothing is perfect. The above tips are only rule of thumbs with numerous of edge cases.

For example:

- You may not be able to easily write a test case that uses the same environment variables and databases as the production environment.
- If you can rerun the program quickly (like in a Jupyter Notebook), then you may be able to get away without automated testing.
- Using new tools may be better in the long-term.

### Other Notes

- The goal isn't to become a faster programmer immediately. One should slowly gain experience, build habits, and
    learn theory to improve.
    - The reason a lot of more experienced programmers don't code quickly is because they have bad habits. For example, they 
      may have too much knowledge and not know how to stop at the right code reliability level.
- It may not pay off to focus solely on coding more quickly.
    The general consensus in industry is that
    new programmers don't write code that is reliable and maintainable enough.
- Bugs generally occur at the non-code level. For example, the overall design of the solution may be
    too slow for the customer or the solution uses packages that can't be used in production. Bugs also tend
    to consolidate around places where work is split between people (integration points).
    -   If you want to code
    quickly while writing good code, you should aim to be careful at those points. Write your integration and
    end-to-end tests. Invest some time to understand what the PM and users want. If you notice an issue with the design
    while coding, bring the issue up to others.
- It rarely pays off to argue with others about your code. Often you should just do what the team
    wants. This doesn't mean being a pushover, you should defend yourself when needed.
- Other things: stay focused, don't get distracted while your code compiles or your tests run.