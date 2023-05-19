---
title: Week 3.1 - Firewalls, Port Scanning and IDS
description: ""
date: 2023-05-19T03:08:41.433Z
preview: ""
draft: false
tags: ""
categories: ""
weight: 0
---
# Firewalls, Port Scanning and IDS:

## Firewalls:
- 1st Generation Firewalls
	- Stateless firewall
	- Packet filters
	- Doesn't track session state information
	- Doesn't inspect traffic
- 2nd Generation Firewall
	- Stateful Firewall
	- Track session state infomation
	- Base for firewall standards
- 3rd Generation Firewalls
	- Stateful Firewall
	- Application Firewalls
	- Deep packet inspection
	- Used where security is paramount

## Port Scanning:
### Nmap:
- Mainly a CLI based tool but there is a GUI front
- Variety of basic and advanced scanning techniques for networks and hosts

## Intrusion Detection Systems (IDS)
- Network Intrusion Detection (NIDS)
- Network Intrusion Prevention (NIPS)
- Host Intrusion Detection (HIDS)
- Host Intrusion Prevention (HIPS)

### IDS Evasion Techniques:
- Players:
	- Masquerader - Where a malicious actor illegitimately poses as an authorized entity to gain access to a system
	- Misfeasor - Where the malicious actor is authorized user but misuses the granted access and privilege
	- Clandestine User - Where a malicious actor who has supervisory control of the system uses this control to evade auditing and access controls or to suppress audit collection
- Evasion Techniques:
	- Fragmentation
	- DOS on IDS
	- Pattern Change
	- Spoofing

## IDS Configuration and Tuning:
- False Positives
- Rules
- Signatures

## IDS Standards:
- IDS Message Exchange Requirement Standard
	- RFC 4766 (IDMEF)
- IDS Message Exchange Protocol
	- RFC 4767 (IDMXP)
