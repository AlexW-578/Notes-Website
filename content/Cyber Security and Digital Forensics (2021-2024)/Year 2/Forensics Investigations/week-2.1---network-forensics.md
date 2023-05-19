---
title: Week 2.1 - Network Forensics
description: ""
date: 2023-05-19T02:54:38.262Z
preview: ""
draft: false
tags: ""
categories: ""
weight: 0
---
# Network Forensics
## Network Capture Tools and Network Logs
- tcpdump
	- -D (lists interfaces)
	- -h (Help)
- Wireshark

### Command line tools
- mergecap - Combines pcap files
- editcap - Manipulates packet capture files
- dnstop - isolates only DNS traffic

### Network Traffic Sources
- Switches - CAM table,direct traffic capture
- Routers - Routing table, Logs
- Firewalls - Vast logs
- Network intrusion detection systems
- Web Proxy servers
- Authentication Servers
- Application Servers

### Network Logs Analysis Methods
- Manual Log review 
	- Manually going through the log files looking for interesting information
- Filtered log review
	- Filtering the log files to make it easier to find information from the logs
- Searching
	- Search through the log files
- Correlation
	- Correlating the logs against known data
- Data Mining

## Scripting
Scripts can be used to automate log analysis and review
- Allows you to focus on specific areas
- Automates the log analysis tasks

### DNS Blacklists
A Common Script that uses regular expressions to filter log files.
it pulls out IP addresses and hostnames from logs and then compares it with another directory to find common items.

## Forensic Reporting
- Fire Department Analogy
	- Take Notes, Record actions, Document decisions and individual contributions
	- Sift through the evidence
	- Same workflow in forensic investigations
- Root Cause analysis
- After-action Review

### Reporting Documentation
#### What to Document?
- Who?
- When?
- Where?
- What?
- Why?
- How?
#### Types of documentation
- Ticketing Systems
- Written Reports
	- Executive Summary
	- Incident Report
	- Forensic Report