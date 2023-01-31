---
title: Intro to the Web
tags:
categories:
date: 2023-01-30
lastMod: 2023-01-30
---
URL's (e.g. http://calcentral.berkeley.edu/academics) have three parts

  + 1. Protocol: "http"
2. Location: "calcentral.berkeley.edu" - this can also include a username or port number
3. Path: "academics" - what resource to request from the server. Can supply key-value arguments after "?" character, like "?key1=value1&key2=value2" and possible anchor which is interpreted by the browser that tells it where in the webpage to go

HTTP:  Operates as series of requests and responses

  + Request types: GET and POST

  + Because it's stateless it relies on cookies to maintain information across requests

Javascript

  + usually sandboxed in browser to prevent attacks

Cookies: Key-value pairs
  + Can have additional metadata - _domain_ and _path_ tell browser which URL to send cookies to, _Secure_ says to only send the cookie over secure connection, etc

  + Browser sends cookie if cookie's `Domain` attribute is suffix of URL domain and cookie's `Path` is prefix of the URL path

    + e.g. cookie with `Domain=berkeley.edu` and `Path=/academics` will be sent to url "https:www.calcentral.berkeley.edu/academics/butthead.html"

      + This doesn't apply to top-level domains like ".com" or ".edu"

    + Not same as [Same-Origin Policy]({{< ref "/pages/Same-Origin Policy" >}}) which can cause problems


