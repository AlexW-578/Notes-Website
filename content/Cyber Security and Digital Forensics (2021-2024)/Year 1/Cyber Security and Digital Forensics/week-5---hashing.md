---
title: Week 5 - Hashing
description: ""
date: 2023-01-08T23:00:02.290Z
preview: ""
draft: false
tags: ""
categories: ""
lastmod: 2023-01-08T23:24:00.303Z
---
# Hashing
Hashing functions allow us to take a variable length input (string, files, or disk) and produce a fixed length output.

## Popular hashing algorithms:
- MD5 (Message Digest 5) 128-bit
- SHA-1 (Secure Hash Algorithm) 160-bit
- SHA-2 (SHA-224, SHA-256, SHA-384, SHA-512)

## Key characteristics
- Given M, it is easy to compute h such that H(M) = h
- Given h, it is hard to compute M (one way property)
- Given M, it is hard to find another message M', such that H(M)=H(M') (Strong Collision Resistance)
- Changing one bit of input changes ~50% of the output bits


