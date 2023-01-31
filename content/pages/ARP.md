---
title: ARP
tags:
categories:
date: 2023-01-30
lastMod: 2023-01-30
---
Address Resolution Protocol - Purpose is to translate IP addresses into MAC addresses

Layer 2 of the internet stack

Original Ethernet was designed to broadcast all messages to machines in local network (machine should just ignore messages that are not meant for it)

ARP Protocol:

  + 1. Broadcast: Send IP address and ask for MAC
2. Response: Send MAC address that corresponds to IP - if IP is outside of LAN the router should respond with its MAC address
3. Cache: Cache mapping

Attack

  + ARP Spoofing: Race to respond to broadcast with incorrect MAC address. Defended by switches which track MAC -> IP address pairings.
