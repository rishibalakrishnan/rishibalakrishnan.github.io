---
title: Same-Origin Policy
tags:
categories:
date: 2023-01-30
lastMod: 2023-01-30
---
Different tabs in browser not allowed to communicate with each other unless they have the "same origin"

Origin is determined by creating a (protocol, domain name, port) tuple and if tuple is the same then two websites have the same origin EXCEPT

  + 1. JavaScript runs with origin of page that loaded it
2. Images have origin of page that it comes from
3. Frames have origin of URL where frame is from
