---
title: TLS
tags:
categories:
date: 2023-01-30
lastMod: 2023-01-30
---
Used to guarantee confidentiality, authenticity, and integrity in internet communications

Built on top of TCP

Protocol

  + 1. Client sends nonce and list of encryption protocols it supports
2. Server sends nonce, selected encryption protocol, and server's public key signed by a certificate authority
3. Generate Premaster Secret known only to client and server - can do this either with RSA or (EC-)DHE. DHE provides forward secrecy unlike RSA because if a private key is discovered later you can't go back and decrypt older messages

Attacks:

  + Replay attack - record TLS communications and send later. Defended against by nonces which ensure that different symmetric keys are generated every time
