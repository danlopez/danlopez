---
title: "Performance tasks for hiring engineers"
date: 2021-10-24T8:51:01-04:00
description: "Why I use them and how to make them effective"
tags: 
    - hiring
    - engleadership
---

A lot of engineers are staunchly opposed to the idea of a performance / take home task in the hiring process, and I get it. They can be time consuming, they're often scoped incorrectly, and it can be hard to imagine that the hiring team spends anywhere near the amount of time on it that you did. There are also equity issues with take home tasks - not everyone *has* a huge amount of time to spend working on these. For tasks with an unenforced time limit, going over the time limit can often lead to vastly better results, biasing the instrument. All of that said, I absolutely think there's still a time and a place for them, as long as they're done deliberately. 

So, when is a performance task appropriate? In terms of timing, it shouldn't be done before you've spoken to a candidate at least once. If you're the hiring manager and you're doing your own phone screens, you can give a candidate a performance task right after the phone screen. If you're relying on recruiters to do a phone screen, you should make sure a technical member of the hiring team finishes a phone screen before jumping into a task. They take too much time for candidates for it to be reasonable otherwise; you want to make sure they are a really good candidate before asking them to spend up to 4 hours on a task. You should assume anyone you're giving a performance task to is someone you'd want to have do a final round interview.

The second thing to consider is just how much your role would benefit from a performance task. I'll get into this later, but a well designed performance task will mimic the actual work that an employee will be doing. Generally, this means that performance tasks are easier to write for lower level roles. Personally, I use them for junior and mid-level roles but haven't used them for senior roles and higher. This is partially because the work a senior does varies quite a bit more, but also because it's easier to evaluate an applicant's past work and contributions at the senior level. 

For the actual performance tasks themselves, I try to ask myself the following questions when I'm developing them: 
1. How can I best mimic the work that they will be doing? (Note that this also applies to technical interview questions)
2. Does this task lead itself to a good discussion during a final round interview?
3. If someone spends extra time on the task, will they do much better?
4. How can I set clear expectations for the task?

For the first, I often try to find a recently developed feature or task that this role would be responsible for. For a backend engineering role, it might be implementing a new set of API endpoints or designing a data model. I try to make sure the task is very well specc'ed out - if we're asking for an API, it should say exactly what features to include, have good descriptions of the data model, etc. I usually don't provide a starting repository to clone here, as I believe that new programming languages can be picked up pretty quickly and would rather someone work where they are most comfortable - I don't want a python developer to feel like they need to learn .NET just for a performance task.

For an SRE role, I like to set up an empty AWS account with a number of sub-optimal configurations (e.g, resource usage, security, networking, application infrastructure). I grant candidates read only access and ask them to audit the account and produce an email with recommendations. This is fairly typical of the tasks they'd have to do on the job - helping developers build new resources (a.k.a cleaning up after them), etc.

The discussion is a hugely important piece. You should plan to spend a full technical interview (30-60 minutes) reviewing the performance task with the applicant. Ideally this feels like a 'design review' process and is highly collaborative. You're trying to get a feel for how they think and work, and whether they would fit in well on your team. You can also use this time to push on the edges of the work they did and see how far their knowledge goes in a variety of different areas. You asked them to write an API? Maybe ask them how they would deploy it or monitor it. 

For all of my tasks, I ask that applicants write out what they would have done if they had more time. It's often infeasible to write unit tests in a 4 hour block, or authentication / authorization, logging, etc, but it helps to know that they're aware of the need to do. 

I can't stress enough how important it is to set clear expectations. This applies to the time limit and to the deliverable itself. If you want someone to write code and submit it on github, either come prepared with a repository for them to submit to or explicit instructions on how to set up a private repo and share it with your hiring team. If you are asking them to write an interface, make sure that there are clear requirements in place (unless part of the performance task is dealing with uncertainty, but this should be deliberate and central to the task, then). 

Finally, be flexible! Ask for it to be done on a certain - reasonable - timeline, but let candidates tell if you that doesn't work for them. You should always give at least a week to complete a 4 hour task, people need time to plan things like this. 

I've hired some great candidates by using this process. While I can't guarantee it - hiring is always hard, no matter how many reps you get, especially for mids & juniors - I think performance tasks help you do a better job quickly answering the most important question: is this person able to do the work and are they someone you and your team wants to work with. 