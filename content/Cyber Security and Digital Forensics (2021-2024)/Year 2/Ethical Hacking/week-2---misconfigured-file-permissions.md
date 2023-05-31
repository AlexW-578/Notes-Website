---
title: Week 2 - Misconfigured File Permissions
description: ""
date: 2023-05-19T02:59:40.143Z
preview: ""
draft: false
tags: ""
categories: ""
weight: 0
---

- Everything within Linux is a file

- File permissions can cause unauthorized users access to the contents of files
  - Meaning that the contents could be changed
  - e.g. Changing the hard coded binary passwords with a known password
  - This breaks confindentiality, Integrity, and availability

## Commands

- Export PATH=/path/to/directory
  - Changes the path variable
- find
  - Search for files in a directory
- locate
  - Find files by name, quickly
- which
  - locate a command

## File Permissions

### User Roles:

- U: User
- G: Group
- O: Others

### Permissions:

- R: Read
- W: Write
- X: Execute

#### Set User identidy (SETUID/SUID)

If there is an 'S' in the file permissions, it is a special permission for the user access level and always executes as the user who own the file. - chmod u+s \<file/dir\>

#### Set Group Identity (SGID)

Allows a file to be executed as the group owner of the file - chmod g+s \<file/dir\>

#### Sticky Bit

Restricts the deletion at directory level - chmod o+t \<file/dir\>

- U - User
- G - Group
- S - SUID

### Commands

- chmod \<Permision\> file
  - Change file permissions
- chgrp \<Group/GID\> file
  - Change group ownership of a file
- chown \<User/UID\> file
  - Change User ownership of a file
- sudo \<command\>
  - Run the command as the root user

## Useful Links

[chmod Calculator](https://chmodcommand.com/)
