---
title: Week 3.2 - Deception Technology and Honeypots
description: ""
date: 2023-05-19T03:09:11.632Z
preview: ""
draft: false
tags: ""
categories: ""
weight: 0
---

# Deception Technology ad Honeypots

## What is Deception Technology?

"Deception technologies are defined by the use of deceits, decoys and/or tricks designed to thwart, or throw off, an attacker's cognitive processes, disrupt an attacker's automation tools, delay an attacker's activities or detect an attack. By using deception technology behind the enterprise firewall, enterprises can better detect attackers that have penetrated their defenses with a high level of confidence in the events detected. Deception technology implementations now span multiple layers within the stack, including endpoint, network, application and data."
[Gartner Identifies the Top Technologies for Security in 2017](https://www.gartner.com/newsroom/id/3744917)

## Why Deception?

- Pro-active Cyber Defense
- Profile Adversaries / Threat Inteligence
  - High or Low skill?
  - Their methods
  - What is of interest?
    - IP
    - Financial data
    - Personal records
    - Everything
  - Waste the time of the adversary.

## Is it legal?

- Entrapment
  - Intelligence gathering, not evidence gathering
- Privacy
  - The only activity touching the deception assets should be illicit activity
- Howerver, some country's laws do not allow for the 'intent' to deceive

## Honeypots

- Allows you to bait and investigate attackers
- Is a whole network setup to invite atttack, that is comprised of multiple honeypots
- Production Honeypots - Design 1
  - Corporate enviroments
  - Placed inside critical infrastructure
  - Limited data capture
- Research Honeypots - Design 2
  - Used for intelligence gathering (Threat intelligence)
  - Capture extensive data for analysis

### Types of Honeypots:

- Pure Honeypots
- Low interaction honeypots
- High interaction honeypots

### Behavior:

- Port scanning
- SSH - scan large blocks using brute force
- HTTP - scan for web app vulnerabilities
  - wordpress, CMSes, forums, etc
- Automated attacks on other systems
- Save access creds and sell them
- Download malware (e.g.) bot and run it
- Use as a malware command and control (C&C)

### Honeypot Tech

#### Kippo:

- Designed to log brute force attacks and shell interaction
- No longer under active development
- Forked to Cowrie

### Cowrie:

- Cowrie was forked from kippo
- Install covered in a in lab exercise
