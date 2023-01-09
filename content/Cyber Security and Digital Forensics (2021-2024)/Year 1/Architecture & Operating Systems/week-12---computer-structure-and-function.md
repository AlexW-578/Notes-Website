---
title: Week 12 - Computer Structure and Function
description: ""
date: 2023-01-08T21:44:31.017Z
preview: ""
draft: false
tags: ""
categories: ""
weight: 1
lastmod: 2023-01-09T00:16:10.697Z
---
# Computer Structure and Function
- Computer Architecture -> Those attributes that have a direct impact on the logical execution of a program.
- Computer Organisation -> Refer to operational units and their interconnections that realise the architectural operation.

## Computer Functions
- Data Processing
- Data Storage
- Data Movement
- Control

![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220531162002.png)

- Data Processing
	- ![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220531165936.png)
- Data Storage
	- Short-Term
	- Long-Term
	- ![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220531170033.png)
- Data Movement
	- Input / Output (I/O)
	- Peripheral
	- Data Communication
	- ![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220531170527.png)
- Control
	- ![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220531170553.png)

## Computer Structure
## Top Level
- Central Processing Unit (CPU)
	- Controls the operation of the computer and perform its data processing.
- Main Memory
	- Where the data is stored.
- I/O
	- Input / Output devices like keyboards, Monitors ,etc.
- System Interconnection (Buses)
	- The communication between the above 3.

![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220531170823.png)


## CPU 
- Control Unit
	- Send signals that control different components of the computer.
- Arithmetic & Logic Unit (ALU)
	- Performs the computers data processing function.
- Registers
	- The internal memory of the CPU
- CPU Interconnections
	- Provides communications between the components within the CPU

![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220531173224.png)

## First Generation
### ENIAC (Electronic Numerical Integrator And Computer)
- World War II
- University of Pennsylvania
- 30 Tons
- 1500 sq. feet 
- 18000 Vacuum tubes
- 5000 Additions per second
- Decimal (Not Binary)
- Manual Programming

| Pros | Con |
| ---- | --- |
|      |  Manual Programming   |

### Von Neumann Machine
- Stored-program concept
- IAS (Institute of Advanced Study) computer
- 1946-1952
- Binary

| Pros | Con |
| ---- | --- |
|   Program stored in data   |     |

## IAS Computer Structure

![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220531174421.png)

### Memory in IAS
- 1000 Locations
- Words (40 bits) - Binary)
	- Number words
		- Sign magnitude
	- Instruction words
		- Has both left and right instructions
			- Each 20 bits long
			
			- 0-7 bits = Left Opcode
			- 7-19 bits = Left Address
			
			- 20-17 bits = Right Opcode
			- 28-39 bits = Right Address

![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220531175134.png)


## Videos:
- [Computer Structure and Function](https://youtu.be/TWRse5BMCvk)

[](Week 13 - IAS Computer)