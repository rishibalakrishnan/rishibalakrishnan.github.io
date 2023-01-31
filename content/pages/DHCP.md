---
title: DHCP
tags:
categories:
date: 2023-01-30
lastMod: 2023-01-30
---
<iframe src="https://textbook.cs161.org/network/dhcp.html" style="width: 100%; height: 400px"></iframe>

Connecting to network requires IP address, IP address of DNS server, IP address of router

DHCP Handshake:

  + 1. **Client Discover**: Broadcast Request for config

  + 2. **Server offer**: Server responds with potential configuration. This often comes with a *lease* after which the client must rebroadcast request for configuration or server frees settings (like IP) for use by another client

  + 3. **Client request**: Client broadcasts which config it's chosen

  + 4. **Server Acknowledge**: Server confirms that its config has been chosen

Network Address Translation: More devices than IP addresses and not all networks support IPv6 (which allows for more IP addresses) -> Multiple devices in same network can share IP addresses.
  + Router assigns device placeholder IP (invalid address on wider internet) and caches this internal IP address to destination of request. Creates actual IP address for device, so that it can return response to correct device

Vulnerability: Spoofing. Malicious server can broadcast bad config settings

  + No real defense except for relying on higher layers and encryption
