---
title: "About this site"
date: 2021-10-05T12:30:00-04:00
description: "Where do the packets come from?"
tags: 
    - raspberrypi
    - infrastructure
---
*Edited 10/11 to account for dynamic DNS*

This site exists because I happened to have an extra raspberry pi sitting around that I wasn't using and thought it would be fun to host a super lightweight, performant site on it. Is this the cheapest way I can do things? No... because GitHub pages is free. But it's more fun!

After talking to my ISP and confirming that they are ok with it - which was really, really lucky, because most ISPs explicitly don't allow it - I stood things up. 

The stack this site is built on: 

* raspberry pi 4 running raspbian
* nginx
* built using hugo & simple.css
* deployed on the same raspberry pi using a self-hosted github action
* noip [dynamic dns](({{< relref "/blog/dynamic-dns" >}} "dynamic dns"))
* wifi, because my router is in a poor location. 

More to come in the future as I think about failover in the event of a power outage, dynamic IP addresses and more. 