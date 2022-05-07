---
title: "Context Matters"
date: 2022-05-07T13:20:44-04:00
description: "Every team is different. Do what's right for yours, not theirs."
draft: true
tags: 
    - engleadership
---


Over the past 10 years, I've worked as an engineering leader at a small startup (under 5 engineers and growing), a mid-sized public company (~350 engineers), and a local government (15 engineers on my team and about 50 in the enterprise). As an engineer, I have a strong tendency to pattern match and implement similar systems in each organization. I've learned over and over again that while this mindset can be positive, there can also be significant drawbacks if not done very deliberately. While you should always be open to making changes, you should also always ask _why_ things are done the way they are and make sure that any changes you are making are appropriate within the context of your new organization. If you take this to the logical extremes, this becomes obvious - what works at Google and Facebook does not work at a 3 person startup. This is true for technologies, process, and people.

When I first began working at the City of Philadelphia, I'd just come from a mature engineering organization that was deeply focused on uptime, reliability, and our "Non-Functional Requirements" (NFRs). The NFRs included items like test coverage, monitoring, documentation standards, internationalization, accessibility, etc. In my first weeks at the City, I looked over our services and saw gaps in all of these areas. I decided to implement a set of NFRs that was almost the same as the one I'd used in the past. I wrote a Standard and got it approved by leadership and started telling engineers in my org and in other d that this was our new standard. Six months later... there was progress, but not much. I stepped back and tried to understand what I was missing and a few things dawned on me.

I realized that the teams and services I was responsible for at the City were very different than the teams I'd run in the past. A few of the main areas where this diverged: 
- The number of services / applications my teams were responsible for. In the past, I had feature teams working on a single Product. At the City, we operated more like an agency, with an appplication : engineer ratio greater than 1:1. 
- We didn't have the same personnel surrounding our engineering group - engineers were operating as Product Managers, Designers and more.
- The audience we were serving was fixed - with 1.6 million residents in the City of Philadelphia, hypergrowth was never something we needed to really consider. 
- Our audience was also very different - in government Digital Services, our users don't have a choice and _have_ to use our services. 

Once I realized just how different the context was, I was able to work with my team and my leadership to prioritize where we spent our time. We decided that our priority NFRs would be monitoring and alerting, CI / CD and accessibility. Monitoring and alerting was an easy area to focus on - we'd often find out about outages from the public. A11y was obvious as well given a recent increase in lawsuits against non-compliant sites. CI / CD wasn't as obvious, but we were able to make it another focus area due to painful deployments processes for a number of existing applications. CI / CD also helped us show developers that we were thinking about them with these changes and wanted to make their lives easier.

By focusing on this smaller subset of NFRs, everything became more attainable. We added a health check endpoint to every service and implemented PagerDuty for alerting. We also wrote a standard Terraform module to migrate our applications to a serverless platform in ECS Fargate - with autoscaling in place so that services would be self-healing, which resulted in us almost never being paged. This standard application architecture also included CI / CD on GitHub actions, making it easy for developers to deploy changes to all environments (which, by the way, were now easy to spin up due to our standard Terraform). 

Accessibility was a bit different to approach - this involved writing standards, training staff and updating our RFP process - and really deserves its own post.

By focused on only a few of these areas, given our resource constraints, we were able to achieve significantly greater success. In retrospect, our organization was _very different_ than where I had been coming from. We had tiny teams that wore a number of hats and simply were not able to re-focus on NFRs on top of existing priorities - and had they done so, it would have been detrimental to our work delivering services to residents. While the NFRs were important, they were not the most important business outcome for our organization.  

This was an easy example, but I've seen this pattern play out again and again in my career - I (or another leader) come in with assumptions about what will work, try something out and it's wrong for the organization. When this happens, you can either question, iterate and strengthen the org, or suffer the consequences of misalignment, underperforming teams and unhappy engineers. Your job is to ruthlessly prioritize what's best for your organization - taking in what you've done before, what you read about on Twitter and Hacker News - and question what works and make it fit. 

--- 
As always, reach out on [Email](mailto:hi@danlopez.fyi), [LinkedIn](https://www.linkedin.com/in/danlopez1), [Twitter](https://twitter.com/lopezbraus) if you'd like to discuss. 