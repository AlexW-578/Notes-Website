---
title: Week 2 File Systems NTFS
description: ""
date: 2023-01-08T23:40:50.022Z
preview: ""
draft: false
tags: ""
categories: ""
lastmod: 2023-01-08T23:48:39.397Z
---

# NTFS File system

- Created for Windows
- Boot Signature 0x55 ⇾ 0xAA
- NTFS created by Microsoft in 1993

## Partition table

- 16 bytes
  - 1st byte = 0x80 bootable/active, 0x00 inactive
  - 2-4th bytes = Cylinder-Head-Sector (CHS) of the first absolute sector in partition
  - 5th byte: partition type (0x0E = FAT 16; 0x0C = FAT 32; 0x07 = NTFS)
  - 6-8 bytes: CHS address of the last absolute sector in the partition
  - 9-12 bytes: Logical block addressing of the first absolute sector in the partition
  - 13-16 bytes: Number of sectors in partition

## NTFS partition organization

- Boot sector
- Master file table
- File system data
- Master File table copy
