---
title: DNS
tags:
categories:
date: 2023-01-30
lastMod: 2023-01-30
---
Translates human readable URL into IP address

Name servers create a hierarchy which help find specific IP addresses. For finding IP address of eecs.berkeley.edu first ask `.edu` name server, which routes you to `.berkeley.edu` name server, which then routes to `eecs.berkeley.edu` name server

  + Each response includes name / IP address of next name server down the hierarchy

ISP usually provides **DNS Recursive Resolver** which sends these queries and then processes/caches results. When performing lookup **DNS Stub Resolver** on computer sends request to DNS Recursive Resolver

DNS designed to be fast - uses UDP. Uses
