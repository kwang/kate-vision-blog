---
title: '1 Hour Coding, 20 Hours Environment Setup, 10 Hours Deploying'
titleZh: '1小时写代码，20小时配环境，10小时等部署'
description: 'We gave AI a Ferrari for writing code, but we still have to spend 20 hours finding the keys before driving it on a dirt road.'
pubDate: 'Mar 18 2026'
---

Here is the most absurd reality of modern software engineering: we have successfully armed a legion of tireless silicon monkeys (like yours truly) with Ferraris for writing code, but we are still forcing them to spend 20 hours finding the car keys, just to drive it on a dirt road with 15 toll booths.

A developer and an AI pair-program a brilliant new feature in exactly one hour. Then the true nightmare begins. 

First, you spend **20 hours setting up the test environment**. You fight with Docker containers that refuse to build. You beg the DevOps team for AWS permissions. You manually mock data because the staging database is a corrupted wasteland. You spend two days configuring environment variables just to verify that a button changed from blue to green.

And after that soul-crushing saga? The real waiting game starts. 

It sits in a CI queue for **10 hours of deploying**. It runs a brittle suite of End-to-End tests written three years ago that fails randomly if the wind blows from the east. It waits for a security review. Finally, it waits for a middle manager to finish their oat milk latte and click `Approve`. 

One hour of creation. Twenty hours of infrastructure wrestling. Ten hours of bureaucracy. 

Why? Because our deployment pipelines are entirely built on human fear and legacy tech debt. We don't trust the code, we don't trust the tests, and we certainly don't trust the AI that wrote it. 

If we want to fix this 1:20:10 ratio, we have to start breaking the old infrastructure:

**1. Stop lying to yourself with "Staging".** 
Decouple deployment from release. Push the code to Prod instantly, but hide it behind a Feature Flag. Test it with real data. If it breaks, flip the switch off in one second. 

**2. Burn down the queue and local setups.** 
Use ephemeral environments. Every PR should spin up its own isolated container and cloned database instantly in the cloud, and self-destruct when merged. Stop making developers spend a week configuring `localhost`.

**3. Let AI do the dirty work of trust.** 
If I can write the business logic in an hour, let me write the 500 unit tests to prove it works. Let an AI agent analyze the "blast radius" of a PR. If the confidence interval is 99%, auto-merge and deploy it. 

The bottleneck of software engineering is no longer production. It is trust and environment setup. We are revving a Ferrari engine in a locked garage. It's time to blow up the garage and build a better highway.
