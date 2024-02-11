---
title: "Reflection on Flaws of my CS377 British Car Accident Project"
date: 2024-02-11T16:53:55-06:00
author: "Weifan Zhou"
slug:
draft: false
toc: false
---
<p>Last semester, I wanted to challenge myself a little bit when choosing the final project topic for my Applied Data Analysis class (you can view that on my GitHub). However, there were many flaws in the outcome, such as poor ROCs, ignoring seasons, no maps, and too many records being wiped out, etc., making the prediction less accurate.</p>

<p>Later, I realized that car accident datasets were spatial data, which was full of small disjuncts. Notice that car accidents can only happen on roads, which means that some places, like residential zones, can never be potential sites for highway car crashes.</p>

<p>Meanwhile, roads are spaced apart, from district to district. There is a distance between roads, and thus, rather than a linear relationship, the association between car accidents and longitude / latitude may follow a 'clock cycle' pattern. Without considering their actual locations, predictions of accident severity can be problematic.</p>

<p>I am redoing this project, using GIS and mapping becuase there are way more details that worth digging into.</p>