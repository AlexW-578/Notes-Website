---
title: Week 3 - Virtualbox
description: ""
date: 2023-05-19T02:49:02.324Z
preview: ""
draft: false
tags: ""
categories: ""
weight: 0
---

## Different Types of Virtual Hard Disks

In the Hard disk section there are multiple options for the hard disk files these are:

- VDI (VirtualBox Disk Image)
  The VDI format was created by Oracle VM Virtualbox as its own container format for virtual hard disks.

  - This format supports both fixed and dynamically allocated storage.
  - It also has a high level of redundancy meaning that there is a reduced risk of data loss.
  - The downside of this format is that it does not support incremental backups and can be slower than VMDK.

- VHD (Virtual Hard Disk)
  The VHD format was created by microsoft and introduced into windows server 2012.

  - Supports both fixed and dynamically allocated storage.
  - Has a storage limit of 2TB.
  - Supports easy undo and redo of any changes that were made to it
  - Supports Multi-user Isolation

- VMDK (Virtual Machine Disk)
  The VMDK format is used by VMware applications.

  - Supports both fixed and dynamically allocated storage.
  - Supports incremental backups
  - Supports snapshots and continuous data protection
  - Can recreate and restart a VM from just the vmdk file

- HDD (Parallels Hard Disk)
  The HDD format is used by Parallels. This is mainly used on macOS.

  - Virtualbox only supports HDD version 2

- QCOW (QEMU Copy-On-Write)
  This format is undocumented in virtual box but the format is used by QEMU.

  - Supports zlib compression
  - Supports Multiple VM snapshots

- QED (QEMU enhanced disk)
  This format is undocumented in virtual box but the QED format is an old QEMU disk image format.

  - Supports backing up files
  - Support for compact image files


## Networks

## UnAttended Install
