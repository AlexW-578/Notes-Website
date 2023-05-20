---
title: Week 2 - VMware
description: ""
date: 2023-05-19T02:48:46.527Z
preview: ""
draft: false
tags: ""
categories: ""
weight: 0
---

## UnAttended Install


## What are the benefits of VMware Tools?

The benefits of VMware Tools is that it greatly improves the experience on a virtual machine by eliminating some issues and adding some features.

A list of the changes created by (VMware. Inc, 2020):

- Low video resolution
- Inadequate colour depth
- Incorrect display of network speed
- Restricted movement of the mouse
- Inability to copy and paste and drag-and-drop files
- Missing sound
- Provides the ability to take quiesced snapshots of the guest OS
- Synchronises the time in the guest operating system with the time on the host

VMware Tools also includes these components:

- VMware Tools service
- VMware device drivers
- VMware user process
- VMware Tools control panel

## Networking

### Subnets

| Class | Public Range                | Private Range                 | Subnet Mask (bits) | # of Networks | # of Hosts Per Network |
| ----- | --------------------------- | ----------------------------- | ------------------ | ------------- | ---------------------- |
| A     | 1.0.0.0 - 127.0.0.0         | 10.0.0.0 - 10.255.255.255     | 255.0.0.0 (8)      | 126           | 16,777,214             |
| B     | 128.0.0.0 - 191.255.0.0     | 172.16.0.0 - 172.31.255.255   | 255.255.0.0 (16)   | 16,382        | 65,534                 |
| C     | 192.0.0.0 - 223.255.255.0   | 192.168.0.0 - 192.168.255.255 | 255.255.255.0 (24) | 2,097,150     | 254                    |
| D     | 224.0.0.0 - 239.255.255.255 | N/A                           | N/A                | N/A           | Reserved               |
| E     | 240.0.0.0 - 255.255.255.255 | N/A                           | N/A                | N/A           | Reserved               |

| Special IP Range            |
| --------------------------- |
| 172.0.0.1 - 127.255.255.255 |

### NAT

A NAT Network is a network that is connected using Network Address Translation (NAT). This means that any machines behind connected to the NAT network will use a different subnet to the external subnet.

### Bridged

A Bridged Network means that the VM connects directly to the outside network using the host's network card like a switch. This means that the VM is a unique device to the network.

### Host Only

Host only means that the VM can only communicate with the host and any other VMs that are connected to the host only network. This means that the VMs are isolated within the host machine, without any access to other networks.

### Custom

A Custom Network is a network that can be configured in many different ways depending on the use case. A Custom Network can be connected to one or mor external networks, or it can run entirely on the host machine.

#### Our Script

## Routing

### Steps:

1. Run `yum install quagga`
2. Edit `/etc/quagga/ospf.conf`
3. Edit `/etc/quagga/zebra.conf`
4. Flush All IP tables using `iptables -f`
5. Enable IP Forwarding using `/sbin/sysctl -w net.ipv4.ip_forward=1`
6. Test
   1. Start Zebra using `zebra -f /etc/quagga/zebra.conf`
   2. Start Ospfd using `ospfd -f /etc/quagga/ospfd.conf`
   3. Watch the routing table using `watch route -n`
   4. Test on clients
7. Restart the Zebra service using `systemctl restart zebra.service`
8. Restart the Ospfd service using `systemctl restart ospfd.service`
9. Enable the Zebra service to run at boot using `chkconfig zebra on`
10. Enable the Ospfd service to run at boot using `chkconfig ospfd on`
11. Test on Clients
