---
title: Week 3 - Case Examination
description: ""
date: 2023-01-08T23:41:54.523Z
preview: ""
draft: false
tags: ""
categories: ""
lastmod: 2023-01-08T23:48:49.142Z
---

# Live and Dead examination

## Dead examination

- Dead examination involves checking the suspect machine in a non-booted fashion.
- Case Management software (e.g. FTK/Encase) mounts the suspect's file system - changes are cached by the tool - the analysis remains 'dead'
- Benefits
  - The integrity of the suspect's data is ensured
  - no instant decision is required
  - Analysis can be repeated

## Case management Tools

- Tools that can manage the complete forensics process
  - Process a wide range of data types (e.g. emails); Analyse the registry; decrypt files; crack passwords; and build a report.
  - Reduce the time required to identify and document evidence

## Live Analysis

- Live analysis utilizes the suspect machine in a booted fashion for examination
  - bespoke applications where it is not possible to obtain a (Licensed) Version
  - Understanding how a piece of malware is behaving
  - Case Dependent
- Order of Volatility
  1.  Main physical memory
  2.  virtual memory
  3.  network state
  4.  running processes
  5.  hard drive
  6.  backup media
  7.  external storage
- Tools
  - Regshot
  - WinDirStat
  - net file
  - net session
