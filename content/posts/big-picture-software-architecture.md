---
title: "Seeing the Big Picture with Software Architecture"
date: 2019-02-08T22:58:36Z
draft: false
---

We all love it when that one person in a meeting once again tells everybody to "take
a step back and think about the big picture."
I honestly would be that person for my team projects, but I'm currently stuck playing the role of "socially-incompetent programmer."

As cliche the advice to "think big picture" is, there is a lot of merit to it.
Software projects generally fail not because the source code is terrible,
but because of higher-level issues in the solution design and the management of the project.
Many startups fail due to improper timing and poor product-market fit, rather than lack of technical
expertise. Those with great technical skills often seem to be the worst with managing the big
picture, because often they can get away with problems by just writing better code more quickly.

One interesting way I've started using recently to improve my own work in team projects is
to compare the team to software architectures. By analyzing the tradeoffs of the designs
I've been able to better communicate and organize myself in my own projects.

For example, one of the biggest mistakes I see other students with great technical skills do is wait for others to give them more work.
You can see the issue with this by making an analogy with Apache Spark.

### The Apache Spark Example

Apache Spark is a program where a "leader" tells all of the "worker nodes" what to do.
If the leader doesn't give a worker any work, then they won't do anything.

![Driver-Worker](https://spark.apache.org/docs/latest/img/cluster-overview.png)

Not only is it generally better for your career to be more self-sufficient, but
the habit of waiting on others for work is detrimental to the overall
productivity of the team.

Apache Spark is useful for quickly getting "embarassingly parallel" big data processing jobs done.
This means the scheduler is good for splitting straightforward, long-running tasks among workers.
The driver program analyzes the job beforehand and takes a decent amount of time to devise a plan
to split the data processing job among the workers. Finally, the workers dumbly follow whatever the
driver program tells them to do (filter the data, send processed output to Worker X).

The work that you do, especially if you're an engineer, is never as
straightforward as the task at hand.
You're boss (especially if they are not a manager) also doesn't have the time to devise a flawless plan that you just
execute to completion.

So even if you aren't confident in your abilities and understand that your seniors
know more than you do, you could do better just by proposing things and communicating actively.
Your saving them time by communicating first instead of having them check up on you later.

For example, you could message others a variant of the following:

_Hey, I finished `<COMPLETED_TASK>` early. I'm not confident that it's 100% right but `<DESCRIPTION_ABOUT_WHATS_WORKING>`.
I'm working on `<PROPOSED_TASK>` in the mean time because `<REASONING_FOR_WORKING_ON_NEW_TASK>`. If there is anything else I can
work on please let me know._

Now you are working on something useful instead of waiting around.
Your boss actually has time to come up with something good for you to work on.
More gets done as a result and everybody is happier.

### Conclusion

Even though these types of analogies are a definitely a stretch, I'd definitely
recommend making them if you are also someone who loves software architecture.
It's fun and pretty useful!

_Endnote:_ some other systems concepts I've turned into lessons for myself:

- _Eventual consistency:_ A lot of systems loosen up consistency constraints
    in order to improve performance.
    You could be more productive if you don't check your email so often or go to every meeting.
- _Health checks:_ If a team member isn't responding to messages, maybe they are overworked.
    You could potentially help out the team by doing them some small favors.
- _Partitioning:_ Communication tends to get unwieldy as more people join a team. Making meetings
    smaller and splitting teams into subgroups often makes things easier.