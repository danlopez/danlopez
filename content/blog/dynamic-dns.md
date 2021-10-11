---
title: "Dynamic DNS"
date: 2021-10-11T2:51:15-04:00
description: "Working around your ISP"
tags: 
    - raspberrypi
    - infrastructure
---

I knew that hosting a website behind a residential ISP would lead to some interesting new issues. The first of those is handling Dynamic IP addresses. As many of you are likely aware, the IP address that you get from your ISP is likely to change at any time... a.k.a, is a [dynamic ip address](https://support.opendns.com/hc/en-us/articles/227987827-What-is-a-Dynamic-IP-Address-). 

In my initial plans, I wanted to preserve some flexibility here, so I looked for a domain registrar & dns provider with an API and landed on google domains. I was imagining that I'd write a cron job that checked my IP using everyone's favorite site, icanhazip.com, every minute. If I saw my IP address changing, then I'd run a script that called the google domains API and updated my DNS entry. I got [this far](https://gist.github.com/danlopez/321458afbed68624d6098f8fa05d7cf7), started looking into the google domains API, and then realized that this has probably already been solved much more easily. 

I came across the set of services called [Dynamic DNS](https://www.cloudns.net/blog/what-is-dynamic-dns/), which exists to solve this exact problem.  I ended up registering for noip.com, a free dynamic dns provider, and following the [directions on their site](https://www.noip.com/support/knowledgebase/installing-the-linux-dynamic-update-client-on-ubuntu/) to install the noip client on my raspberry pi. When you install it, their readme provides further instructions for configuring it as a service. I reconfigured my domain to use a CNAME instead of an A record, forward the root to www, and was good to go. 

Next up: let's load test this thing! or maybe talk about how to monitor and failover when we have a power outage.