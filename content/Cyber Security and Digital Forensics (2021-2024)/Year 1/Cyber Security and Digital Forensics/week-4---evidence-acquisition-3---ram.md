---
title: Week 4 - Evidence Acquisition 3 - RAM
description: ""
date: 2023-01-08T22:59:37.395Z
preview: ""
draft: false
tags: ""
categories: ""
lastmod: 2023-01-08T23:23:58.166Z
---
# Evidence Acquisition 3 - RAM

## Live Forensics:
Methodology which advocates extracting the live system data before pulling the plug to preserve memory, process, and network information that would be lost in traditional methods of forensic approach.

### Extracts Live System Data:
- Memory
- Process Information
- Network information
- Does have a minor impact on the machine
- Must Save the data collected to external device

## ACPO Guidelines

### Principle 1:
No action done should change the data which may be relied upon in court

### Principle 2:
If someone needs to access the original data that person must be competent to do so and be able to give evidence explaining the relevance and the implications of their actions


### Why do live forensics?
- Minimal Downtime
- Provides context for static analysis
- Some data is only stored in RAM
- Long data lifetime even after days
- Evolution of enterprise network (Can logon remotely)
- Evolution of data storage


### Evidence in RAM:
- Running processes
- System Information (e.g. time since last reboot)
- Open network connections
- Recent web browsing activities including private mode
- Unpacked/Decrypted version of protected programs
- Webmail & social networking logon sessions
- Running malware/Trojans


### Issues for considerations:
- Legal process
- Integrity (RAM forensics leaves a footprint)
- Destroy evidence (accidentally or by anti-forensics)
- Weigh the risk to the investigation
- Importance/Urgency (info on a bomb threat vs Evidence of fraud)


#### Locked Screen:
- Criminal Investigations (LOW RISK)
	- Ask suspect for password/PIN.
	- Police can forcefully take fingerprints. (Regulation of Investigatory Act 2000)

- Password Attacks (HIGH RISK)

- Network Attacks (HIGH RISK)


#### Order of volatility:

1. Register, Cache
2. Main Physical memory
3. Virtual memory
4. Network status
5. Running processes
6. Hard drive
7. External Storage Media


#### Acquisition:
##### Strategy 1:
Collect all and examine later

##### Strategy 2:
Use Various tools to probe different aspects of the running system
	
Must be on a external device to not contaminate device


