---
title: "What Is an Asg"
date: 2022-03-17T16:56:50Z
draft: false
---
Auto-Scaling Groups (ASGs) are collections of AWS EC2 instances (or versions of the codebase). New ASGs for each service are deployed during each deployment. ASGs are then attached to LoadBalancer target groups, which allows traffic to hit them.

I had deployed code to make a fix, but the error was still occurring even though the change was in master. Turns out there were old ASGs hanging around that had not been deleted, so a version of the old code was still receiving traffic and triggering the old exception.
