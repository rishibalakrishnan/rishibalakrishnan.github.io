---
title: SQL Injection
tags:
categories:
date: 2023-01-30
lastMod: 2023-01-30
---
Process of manipulating inputs to SQL queries to create unintended behavior

  + Usually pass in some mix of garbage input to make sure that the intended query doesn't return anything, as well as other input that has ' or " and ; to start a "new" SQL query within the bounds of the old one

Defense

  + 1. Escaping characters in SQL - issue is that characters can just be escaped twice and then we're back to where we started
2. Parametrized SQL - prepare statements with areas to plug in parameters. The SQL has already been "prepared" (compiled) and then parameters are just plugged in. This stops all SQL injection attacks
