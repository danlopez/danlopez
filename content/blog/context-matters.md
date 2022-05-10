---
title: "Context Matters"
date: 2022-05-07T13:20:44-04:00
description: "Every team is different. One size doesn't fit all for people, technology and process."
draft: false
tags: 
    - engleadership
---


Over the past 10 years, I've worked as an engineering leader at a small startup, a mid-sized public company, and a local government. Whenever I move into a new role, I'm always asked to review the systems in place and set out a plan to improve them. My (and most people's) tendency is to heavily pattern match. Your old company's flavor of agile was a rigid scrum model? Every line of code has to have a unit test? Well, that's what you'll lean towards, along with a combination of practices that Hacker News / First Round Review / FAANG companies write about and tell us are best practices.


 I've learned over and over again that while this mindset can be positive, there can also be significant drawbacks if you don't understand the full context of your new team. While you should always be open to making changes, you should also always ask _why_ things are done the way they are and make sure that any changes you are making are achievable and in alignment with the goals of your organization. If you take this to the logical extremes, this becomes obvious - what works at Google and Facebook does not work at a 3 person startup. This is true for technologies, process, and people.

When I first began working at the City of Philadelphia, I'd just come from a mature engineering organization that was deeply focused on uptime, reliability, and our "Non-Functional Requirements" (NFRs). The NFRs included items like test coverage, monitoring, documentation standards, internationalization, accessibility... all things that I still think are incredibly important. In my first weeks at the city, I looked over our services and saw gaps in all of these areas. I decided to implement a set of NFRs that was almost the same. I wrote a policy, got it approved by leadership and started telling engineers in my org and in other departments that this was our new standard. A few months later... there was progress, but not much. 

I stepped back and tried to understand what I was missing, and I realized that the teams and services I was responsible for at the city were very different than the teams I'd run in the past in a few critical areas: 
- The number of services / applications my teams were responsible for. In the past, I led feature teams working on a single product. At the city, we operated more like an agency, with an application : engineer ratio greater than 1:1. 
- We didn't have the same level of resourcing surrounding our engineering group - engineers were wearing multiple hats, operating as product managers, designers, project managers and more.
- The audience we were serving was fixed - with 1.6 million residents in the City of Philadelphia, hypergrowth was never something we needed to really consider. 
- Our audience was also very different than a company - in government, our users don't have a choice and _have_ to use our services. 

Collectively, this meant that every engineer had less time to focus on everything, each service had fewer engineers, and while scaling was important, there were predictable limits to operate within. Once I realized just how different the context was, I was able to work with my team and my leadership to prioritize where we spent our time. We decided that our priority NFRs would be monitoring and alerting, CI / CD and accessibility. Monitoring and alerting was an easy area to focus on - we'd often find out about outages from the public. A11y was obvious as well given a recent increase in lawsuits against non-compliant sites. CI / CD wasn't as obvious, but we were able to make it another focus area due to painful deployment processes for a number of existing applications. CI / CD also helped us show developers that we were thinking about them with these changes and wanted to make their lives easier.

By focusing on this smaller subset of NFRs, everything became more attainable. We added a health check endpoint to every service and implemented PagerDuty for alerting. We also wrote a standard Terraform module to migrate our applications to a serverless platform in ECS Fargate - with autoscaling in place so that services would be self-healing, which resulted in us almost never being paged. This standard application architecture also included CI / CD on GitHub actions, making it easy for developers to deploy changes to all environments (which, by the way, were now easy to spin up due to our standard Terraform). The other major bonus for this approach was that we were able to share this work across all of our services, allowing it to operate as a force multiplier.

Accessibility was a bit different to approach - this involved writing standards, training staff and updating our RFP process - and really deserves its own post.

By focused on only a few of these areas, given our resource constraints, we were able to achieve significantly greater success. In retrospect, our organization was _very different_ than where I had been coming from. We had tiny teams that wore a number of hats and simply were not able to re-focus on NFRs on top of existing priorities - and had they done so, it would have been detrimental to our work delivering services to residents. While the rest of the NFRs were important, they were not the most important business outcome for our organization.  

This example was something that I had direct experience with, but it's even more important that you question the context when you are trying to apply patterns that you've only read about, or that are in drastically different organizations (e.g, going from FAANG to local government). It's always good to learn from others, but taking the nucleus of their ideas and fitting them to your organization works a lot better than applying blog post XX as is. 

In general, I've seen this pattern play out again and again in my career - I (or another leader) come in with assumptions about what will work, try something out and it's wrong for the organization. When this happens, you can either question, iterate and strengthen the org, or suffer the consequences of misalignment, underperforming teams and unhappy engineers. Your job is to find the right changes for your organization _given the context that you work in_. 

A few other examples you should be questioning, which might become future posts:
- Flavor of agile - kanban v. scrum v. a 'pick and choose what works'.
- Technical infrastructure for your web application (k8s, ecs, lambda, etc.)
- Hiring process
- Engineering 'profiles' (e.g, what makes a Sr. Software Engineer at your company)

--- 
As always, reach out on [Email](mailto:hi@danlopez.fyi), [LinkedIn](https://www.linkedin.com/in/danlopez1), [Twitter](https://twitter.com/lopezbraus) if you'd like to discuss. 