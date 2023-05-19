---
title: Week 4 - Active Infomation Gathering
description: ""
date: 2023-05-19T03:00:19.079Z
preview: ""
draft: false
tags: ""
categories: ""
weight: 0
---
# Active Information Gathering
## Port Numbers:
### Common Ports:
- 80 - HTTP
- 443 - HTTPS

## TCP:
| Client | Connection | Server  |
| ------ | ---------- | ------- |
| SYN    | ->         |         |
|        | <-         | SYN-ACK |
| ACK    | ->           |         |

### SYN Scan:
Open Port:
| Client | Connection | Server  |
| ------ | ---------- | ------- |
| SYN    | ->         |         |
|        | <-         | SYN-ACK |
| RST    | ->           |         |

Closed Port:
| Client | Connection | Server |
| ------ | ---------- | ------ |
| SYN    | ->         |        |
|        | <-         | RST       |

### Connect/Vanilla Scan:
Open Port:
| Client  | Connection | Server  |
| ------- | ---------- | ------- |
| SYN     | ->         |         |
|         | <-         | SYN-ACK |
| ACK-RST | ->           |         |

Closed Ports:
| Client | Connection | Server |
| ------ | ---------- | ------ |
| SYN    | ->         |        |
|        | <-         | RST       | 

## UDP:
### UDP scan:
Open Ports:
| Client | Connection | Server |
| ------ | ---------- | ------ |
| UDP    | ->         |        |
|        | <-         | NO RESPONCE       |

Closed Ports:
| Client | Connection | Server |
| ------ | ---------- | ------ |
| UDP    | ->         |        |
|        | <-         | ICMP Error       |

### ICMP scan:
Open Ports:
| Client | Connection | Server |
| ------ | ---------- | ------ |
| FIN    | ->         |        |
|        | <-         | NO RESPONCE       |

Closed Ports:
| Client | Connection | Server |
| ------ | ---------- | ------ |
| FIN    | ->         |        |
|        | <-         | RST       |

## Other Scans:
-   Xmas Scan
-   Null scan
-   TCP ACK scan
-   Idle scan
-   FTP bounce scan
-   Fragmented scan
-   Strobe scan
-   Windows scan
-   Service fingerprint scan


## NMAP:

### Preventitive Measures:
- Firewalls
	- Custom Rules (Block unwantedports/IPs)
	- Block ICMP
- IDS/IPS
- Update firmware/OS/patches
- Test networks
- Reverse Proxy

## Service Enumeration:
-   Enumeration is the systematic process of gathering information about a target machine by actively connecting to it.

Service Enumeration is able to collect:
	- User Accounts
	- Network Map
	- Ports
	- Services
	- Credentials
	- Guest Logins
	- Policies
	- etc


## Banner Grabbing:
Most services will give you a banner when connecting to it. So banner grabbing is getting that banner as it can give infomation about what softwere is running on tha machine.

### Protective Measures:
-   Disable banners (or use fake)
-   Disable unnecessary services
-   Some lockdown tools/plugins available
-   Filter in an application gateway (proxy)
-   Hide file extensions (application mapping)
-   Override default error messages

### Vulnerability Scanning:
