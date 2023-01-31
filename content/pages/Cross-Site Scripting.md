---
title: Cross-Site Scripting
tags:
categories:
date: 2023-01-30
lastMod: 2023-01-30
---
aka XSS

Basically the insertion of Javascript into some webpage such that when the webpage is loaded the javascript is as well with the origin of the webpage which means that [Same-Origin Policy]({{< ref "/pages/Same-Origin Policy" >}}) can be thwarted

Can either be stored in the webpage or stored within the parameters of a request that the user is tricked into making

Defense:

  + 1. Sanitize - this can be tricky but there is apparently a set of robust sanitization practices

  + 2. Content Security Policy - scripts can only be loaded in from a list of approved domains per web server
