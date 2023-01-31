---
title: Wireless Local Networks_ WPA2
tags:
categories:
date: 2023-01-30
lastMod: 2023-01-30
---
Purpose: Communicate secures in a wireless local network

This is the protocol that's used for wifi that has one password for every user

Has **access point** that's constantly broadcasting beacon packets that contain the name of the network (akak the SSID - service set identifier)

**PTK (Pairwise Transport Key)** used to send messages from device to network and vice versa

**GTK (Group Transport Key)** used to broadcast messages to the entire network

WPA2-PSK:

  + 1. Client makes authentication request
2. Both client and access point derive PSK from password
3. Access point sends nonce and client derives PTK from nonce, password, and MAC addresses
4. Client sends nonce and MIC and AP derives PTK from PSK, nonces, MAC addresses
5. AP sends MIC and encrypted GTK
6. Client sends ACK

Attacks:

  + Everything is sent unencrypted except for GTK. On-path adversary can learn nonces and MAC addresses. If attacker part of Wifi network, they can also derive PTK. If not, they can brute force PTK by trying different passwords and checking whether they result in same MIC

Defense:

  + WPA2-Enterprise: Each user gets different password. Before handshake, client connects to secure authentication server using [TLS]({{< ref "/pages/TLS" >}}) and provides username and password. If authentication successful, the server presents client and access point with **Pairwise Master Key** which is then used in handshake instead of PSK

  + 
