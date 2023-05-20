---
title: Week 5 - Adder - Subtractor
description: ""
date: 2023-01-08T20:02:22.047Z
preview: ""
draft: false
tags: ""
categories: ""
lastmod: 2023-01-08T23:18:57.163Z
---

## Addition

### Half-Adder

![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220531155902.png)

#### A+B

| A   | B   | Sum | Carry |
| --- | --- | --- | ----- |
| 0   | 0   | 0   | 0     |
| 0   | 1   | 1   | 0     |
| 1   | 0   | 1   | 0     |
| 1   | 1   | 0   | 1     |

Uses an XOR gate for the sum and a AND gate for the carry

If you combine a XOR and a AND gate you can add together 2 bits

### Full-Adder

![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220531160213.png)
![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220531160417.png)

To Add 4 bits together you would need 4 Full-Adders

![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220531160518.png)

## Subtraction

Uses 2s-Compliment

### Steps

1. Flip the bits
2. Add 1
3. Add them together

![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220531160903.png)

## Both Adder and Subtractor

![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220531161111.png)
![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220531161203.png)

\*Put Notes Here

## Videos

- [Adder/Subtractor](https://youtu.be/uz_nTQZzKWM)
