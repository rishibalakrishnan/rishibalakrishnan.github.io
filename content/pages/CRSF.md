---
title: CRSF
tags:
categories:
date: 2023-01-30
lastMod: 2023-01-30
---
Related to implementation of [Cookies](Cookies: Key-value pairs
) and session tokens

  + Basically attacker tricks user's browser into making a GET/POST request with malicious parameters to a website which the user is logged into - the browser will automatically send the session token along with the request which makes the action succeed

Defense

  + CSRF Token - server generates token associated with every form, which is checked on form submission

    + Server needs to maintain mapping of session tokens to CSRF

  + Referer Validation

    + A field which is included in the HTTP headers which indicates which URL the request was made from - these are not always included and can sometimes be filtered out as well which makes them inconsistent


