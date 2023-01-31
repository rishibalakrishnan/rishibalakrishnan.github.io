---
title: IP Routing
tags:
categories:
date: 2023-01-30
lastMod: 2023-01-30
---
<iframe src="https://textbook.cs161.org/network/bgp.html" style="height: 400px; width:100%"> </iframe>

IP address used to uniquely identify devices on whole internet (abstracting away [NAT](Network Address Translation: More devices than IP addresses and not all networks support IPv6 (which allows for more IP addresses) -> Multiple devices in same network can share IP addresses.
) )

  + IPv4 consists of 32 bytes with specified prefix size (e.g. 161.22/16 has prefix size 16) where prefix specifies a subnet and max number of devices on subnet is 2^(32 - prefix size)

  + Some reserved IP addresses (like 127.0.0/24 for localhost)

When sending packet, device first checks whether IP address corresponds to same subnet - if it does, device uses [ARP]({{< ref "/pages/ARP" >}}) to translate IP to MAC address and sends directly

Routing for different subnet consists of **Autonomous Systems (AS)** identified by **Autonomous System Numbers (ASN)** which broadcast their location as well as the autonomous systems that neighbor them that they are able to send packets to. This allows the creation of paths through the entire internet which is how packets are sent. This protocol is called **Border Gateway Protocol (BGP)**

Attacks:

  + Malicious AS - No real defense except relying on higher layers like TCP and their cryptographic protocols like TLS
