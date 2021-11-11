---
title: "Building Developer Communities"
date: 2021-11-11T9:21:11-05:00
description: "Building degrees of community in a disparate organization"
tags: 
    - engleadership
    - cityofphiladelphia
---
*Note: The below is not an official communication of the City of Philadelphia, all opinions are my own*

While we can all agree that engineers hate meetings, we all also know that we work better when we're part of a community. Most engineers want to have colleagues that give thoughtful code reviews, want to participate in a collaborative software design process, and feel supported. Nobody likes the feeling of being the only one that can solve an issue - and more practically, being on call all of the time. 

Building developer community in your organization is absolutely critical for high performing organizations. It will improve developer retention and satisfaction, leading to improved performance and reliability of your services. But, it's not easy to build a collaborative community - especially in an organization like the City of Philadelphia.

## How we're constructed

Like other large municipalities (and, I'm assuming, state and federal governments, some large enterprises, and more), the City is an extremely silo'ed environment. We have over 50 departments within the administration, not to mention a handful of separate row offices like our City Commissioners (our term for board of elections), DA's office, Sheriff's office, City Council and more. Each of these departments historically ran their own IT organizations. A number of years before I landed at the City many of the large departments were "consolidated" and created a matrix structure within the central Office of Innovation and Technology (OIT). Many other departments remain fully silo'ed. 

I lead OIT's software engineering organization, a group of 10-15 developers working on projects ranging from phila.gov to the LHHP database to shared services like PhilaUI. We take on projects with departments, we consult with departments on their own projects both from vendors and developed internally, we review and consult on RFPs and much more. 

At least 10 departments also have their own dev teams, ranging from large teams at some of the largest departments to a lone developer elsewhere. We've attempted to build a community here to bring all of our developers together - but the environment certainly presents some unique challenges. 


## Three tiers of developer community

While our goal is for all developers at the City to feel supported in their mission to produce high quality code and reliable, accessible services for City developers, not everyone is interested and willing to engage. 

### Tier 1: Visibility & standards
The lowest level of community starts with visibility. At central OIT, we want to make sure we know what everyone is building, where their source code lives (ideally in our central GitHub), where their services reside online and whether they are up. We also want to help developers build software that's more secure and better supported when things go wrong. If a department with a single developer loses them and we *don't* know where the source lives, that can present a huge problem. 

This tier is also characterized by standards. At OIT's software team, we work with our Enterprise Architecture team and others in leadership to write and disseminate standards for other developers to follow. These range from accessibility (our a11y strategy is built on WCAG 2.1 AA) to observability and documentation. Our lowest 'tier' of community is the departments that need to be in compliance with standards. Even building awareness of these standards can be a challenge, so we start there - and then we do our best to provide support to developers as they implement these. 

### Tier 2: Shared Services and a "paved path"
The next tier of community we see at the City is developers that share patterns and services. OIT software has worked with departments to develop shared Terraform modules to provision scalable, secure APIs in our cloud environments. We've built a UIKit (PhilaUI) that departments can use to provide accessible, standards compliant interfaces. We have centralized management of monitoring and alerting. We're going to be launching a resident-facing SSO platform to make auth easier to build (and more secure).

We try to work with departments to provide on ramps to using these services. In some cases, it's as simple as opening a ticket. We try (although don't always succeed) to be relentlessly positive and provide developers to pair on these initiatives. 

This approach is generally characterized by the "paved road" approach popularized by Netflix. While we don't mandate using our shared services, we want to make it easiest to achieve our standards by doing so. Teams are free to implement their own solutions as well. 

### Tier 3: Consistent vision and practices
When teams choose to embrace all of our shared services, whether by embedding their developers with us, partnering with us to develop services, or leaning in on their own, we get to our top tier of community. We're using shared tooling, we build apps the same way, we document them in the same places and more. 

When we're at this level, it's easier to provide support and grow together - it's almost like a superpower. We can share code samples, we can debug each other's services and more. While we don't need to bring all departments and groups here to be successful, we think that doing so helps the City deliver higher quality services more efficiently. 

## Our approaches to building community
OK, so the big question here is - how do we take a silo'ed environment and bring people together, providing meaningful opportunities to share ideas and collaborate? 

We start at the team (org level?) level by sharing ideas and patterns. We encourage code review across projects. Our team is often split across a number of different concurrent projects, but we try to make sure that our front-end developers follow similar patterns, share what works and what doesn't, and just know what everyone is working on. Our team at OIT does our best to work in the open - unless we have an explicit reason not to, our source code is shared with all other groups in the City. Our project channels are in the open. When we implement meaningful new patterns, we try to publicly share them on our Confluence pages and in specific channels (we use Teams, but this works on slack too). This **transparency** is a key level in building community. Our goal is that people know who each other are and what they are working on; that way when someone actually needs help they have a head start and feel comfortable working together. 

I mentioned this already so won't go into a ton of detail here, but we also develop - and evangelize - shared services. We do our best to closely suppport any group interested in using these services. 

Finally, a huge part of our community building comes in the form of our regular (often quarterly) developer meet-ups across the City. These meetings - we call them DevXChange, or DevX for short - are the place for teams to share the work they are doing with others, ranging from fully built solutions to shared services they can consume. We've covered topics such as using Google Analytics, implementing login via Azure AD, building APIs on Fargate and much more. We have over 75 regular attendees for DevX and this is the single best way for us to get in touch with developers around the City. DevX is supported by Teams channels and confluence pages. We're constantly pulling new developers into the community, including many that are completely outside of our organization. 

DevX has become a jumping off point for trainings; we've offered wide-reaching trainings on monitoring and observability, AWS services, Git & GitHub, web accessibility and more. We also use DevX as a place for education on new and updated standards. While we could do some of this over email, we find that the best way to get buy-in here is to provide value and support through education, code samples and transparency. 

## What's next?
While we've been building these structures for community for years, we still have a long ways to go. Less than half of City developers leverage our shared services. While all new RFPs now include language around key standards for web accessibility and data access via APIs, the majority of our services aren't hitting our mark. As we continue to prioritize community, we'd like to see more groups of developers self organizing and sharing best practices, designs and more. One of our biggest challenges is a common one in government - we're all drastically under-resourced. While we understand that investments in community always pay off in the long run, it can be hard for us to embrace it in the short-term when we have fires that need to be put out. 

If you're a City developer reading this, please take the time to reach out and get to know your colleagues! 