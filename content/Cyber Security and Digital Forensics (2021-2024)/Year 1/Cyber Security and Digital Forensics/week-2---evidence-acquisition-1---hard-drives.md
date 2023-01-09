---
title: Week 2 - Evidence Acquisition 1 - Hard Drives
description: ""
date: 2023-01-08T22:59:05.091Z
preview: ""
draft: false
tags: ""
categories: ""
lastmod: 2023-01-08T23:23:53.653Z
---
# Evidence Acquisition 1 - Hard Drives

## Methods:
- Acquire image/copy of original evidence
- Authenticate the image
- Analyse the data on the copy only
- Forensic acquisition should be performed correctly, or it may invalidate the results of later analysis

  
## Image variables:

### Storage Technology:
- Spinning disk
- Solid state/Flash
- RAM
- Cloud

#### File System:
- FAT
- NTFS
- HFS+
- EXT
- exFAT

#### Connection to forensic system:
- Firewire
- IDE
- Sata      
- SCSI
- USB

#### Forensic system OS:
- Linux
- Mac OS
- Windows

#### Write Blocker:
- Hardware
- Software

 #### Imaging method
- Hardware
- DD
- EnCase
- FTK Imager

### Imaging:

##### Physical Acquisition:
- preferred method
- Includes slack and unallocated space
- Error Handling

##### Logical Imaging:
- Gets the logical drive
- Many logical partitions per physical drive
- Can be useful in RAID configuration as logical partitions can span multiple drives


### Acquisition Formats:

#### Raw Format (e.g. output from dd):
- Bit by bit copy of drive
- Same size image as original

##### E01:
 - Expert Witness format (Encase format)
 - A container of evidence and metadata (includes hash values)
 - Can be compressed

##### AFF:
 - Advanced Forensic format
 - A container of evidence and metadata

##### Ex01:
- Format for Encase v7
- More extensible than E01
 - A container of evidence and meta data (including Hash values)

### Integrity of Evidence:

#### Write Blocker:
 - These are devices that allow acquisition of information on a drive without creating the possibility of accidentally damaging the drive
 - May also provide drive protection by limiting the speed of the drive attached to the blocker
 - Can be either hardware or software based

##### Hardware Write Blocker:
 - Sits in-between the PC and the storage device
 - Monitors the commands that are being issued and prevents the computer from writing data to the storage device

##### Software Write Blocker::
 - Modified the interrupt table on the PC
 - If another element has control over the controller, then stuff can be written to the device.

#### Hash:
- Use a one-way hash function to create a fingerprint of the data.
- This then can be referred to make sure that the data remains unmodified
- It is one way and cannot be reversed back to the data given to the function.
- Strong collision resistance

