---
title: Week 2.2 - Onion Routing and TOR
description: ""
date: 2023-05-19T03:07:52.646Z
preview: ""
draft: false
tags: ""
categories: ""
weight: 0
---

# The Onion Router

- Anonymiser
  - Hides your IP address by encrypting at each step
- TOR Project
- Sends packets through multiple different routers to reach the final destination
  - Packets are encrypted at each step

## How TOR works (Normallly):

1. Tor client obtains list of TOR entry nodes from a directory Server
2. Tor client picks a random path to destination server
   - All connections are encrypted by tor apart from the connection from the exit node to the server
3. Random paths are selected for every site that is visited

### How TOR works (Bridge)

1. User requests a bridge location from torproject.org
2. User requests a bridge from BridgeDB to provide the bridge
3. Tor client connects to the bridge and then to the wider tor network
4. Tor client obtains list of TOR entry nodes from a directory Server
5. Tor client picks a random path to destination server
   - All connections are encrypted by tor apart from the connection from the exit node to the server
6. Random paths are selected for every site that is visited

#### Why use a bridge?

A bridge is used if tor is being blocked in the network that you are connected to. it also helps to conceal the fact that you are using tor. This is due to the fact that tor bridges are not listed publicly meaning that adversarys cannot identify them easily.

## Tor Browser (Recommened):

- A Seperate browser to your normal browser
- Connects to the tor network
- Only traffic from the browser is sent through tor
  [Tor Browser](https://www.torproject.org/)

## TorGhost:

Tor ghost is a script that redirects all internet traffic through a SOCKS5 tor proxy.
DNS requests are also redirected through tor, thus preventing a DNSLeak.
The script also disables unsafe packets from exiting the system, though some packets like a ping request can compromise your identity.

**This is now archived on github meaning no active development**
[TorGhost](https://github.com/SusmithKrishnan/torghost)
