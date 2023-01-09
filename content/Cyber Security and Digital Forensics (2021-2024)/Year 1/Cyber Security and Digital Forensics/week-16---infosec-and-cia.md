---
title: Week 16 - InfoSec and CIA
description: ""
date: 2023-01-08T23:02:02.462Z
preview: ""
draft: false
tags: ""
categories: ""
weight: 1
lastmod: 2023-01-09T00:17:30.653Z
---
# InfoSec and CIA

## Information Security:
InfoSec is about protecting all information against unauthorized access that could result in undesired data modification or theft.

## Cyber Security:
Cybersecurity refers to the practice of protecting data, its related technologies, and storage sources from threats.


## CIA Triangle:
- Confidentiality:
	The property that information is only made available or disclosed to authorised individuals, entities or processes
	
- Integrity:
	The Property of safeguarding the accuracy and completeness of assets against unauthorised access or modification.
	
- Availability:
	The property of being accessible and useable on demand by an authorised entity


# Encryption
## Keywords:
- Plaintext - Original message to be transmitted
- Ciphertext - encrypted version of the plaintext
- Encryption algorithm - specific recipe for going from plaintext to ciphertext
- Key - additional input controlling encryption/ decryption algorithms.
	- In many cases the key is secret, and without it decryption is impossible.


## Method of encryption:
1. Plaintext
2. Encryption
3. Ciphertext
4. Decryption
5. Plaintext

## Algorithms:
- Algorithm - A detailed set of instructions which results in a predictable end-state

## Symmetric Key Encryption:
- Can be used with both Stream and Block Encryption methods.

#### Examples:
- Vernam Cipher:
	- XORs the plaintext with a key to create ciphertext.
- RC4
	- Designed by RSA in 1987
	- Used in WEP and WPA
	- Generally regarded as insecure but still used as a backup due to its speed and simplicity
	- Makes use of XOR with a key
	- the key was generated using a pseudo-random number generator
	- but it turned out to be not as random as it was presumed to be.
- ChaCha20
	- Used by google for HTTPS
### Block and Stream Encryption:

| Stream Cipher                  | Block Cipher                   |
| ------------------------------ | ------------------------------ |
| Operates on single digits      | Operates on fixed block sizes  |
| Faster                         | Slower                         |
| Continuous processing          | Block by block processing      |
| Less Code                      | More Code                      |
| Needs a new key each time      | Can reuse the key              |
| Wireless communication         | File Encryption                |
| Best implemented with hardware | Best implemented with software |
| Uses Vernam Cipher             | Uses Feistel Cipher            |
| Reversing is easy              | Reversing is hard              |

#### Stream Cipher:
- Encrypts the information a byte or letter at a time.

##### Examples:
###### Caesar Cipher:
- The letters of the plain text are substituted with another letter a set distance down the alphabet.
- An example of a stream cipher.

#### Block Cipher:
- Encrypts information as a single block.
- Generally requires a computer to handle the transformation.
- Generally more efficient.
- The Plaintext is broken into blocks of a specific size
- each block is then encrypted separately(a round)
	- each round is a series of simple steps
- In each round half of the block is altered with a function and a subkey
- Then it is XOR'd with the other half
- These rounds are then repeated
- More rounds = More security but also with more processing load
- Each round has a separate set of keys

##### Examples:
###### DES/Triple-DES:
- Data Encryption Standard
- Old and generally insecure
- Makes use of the Feistel Cipher
- Short key length of 56 bits - Makes it vulnerable to brute force attacks
- Triple-DES is DES but done 3 times
	
Steps:
1. Expansion 
	- 32-bit half block expanded to 48-bits
2. Key Mixing
	- Expanded half block is XOR'd with subkey
3. Substitution
	- Resulting block is broken up into 8 6-bit blocks
	- the S-boxes transform the 6 bits into 4 bits (this part makes it non-trivial)
4. Permutation
	- The P-Box then mixes up the S-Box output so that the outputs are spread out over the next sequence of S-Boxes

	![](https://lh6.googleusercontent.com/H7hW0rrxsnQsQxbrmtEJmKIQzRd85jVe9FK7bv9RISO4OCDqjqDaaUEkl1m95vYTtcMoIoaHCotUXoelBq8h_2rYTNscMJBsHd2NA5_t7YMdbIGXGlxJLxPOUIZshyB4mjNBmAJFJlCe-IeUXA)



###### AES:
- Advanced Encryption Standard
- Very common
- Can be expanded
- Uses a Substitution-Permutation network
	- S-Boxes = Substitute a small block of inputs with another small block
	- P-Box = Permutates the S-Box outputs and feeds them into the next round of S-Boxes
		- Permutation = Rearrangement
		- {1,2,3}, has 6 versions (2,1,3), (2,3,1), etc
		
![](https://lh5.googleusercontent.com/mPhVw4vVIWoOqfd_LzpKMNWUv_opr0ZMpLuJ6GIyuV1NhIFccpdwhy4zXTAD9_4N68iCP3u43K63-01qH5obbBtHGNowsoxB4Uqxh_mea49ymVbFqGqJab44NoYI77XXBmNHIzVHLGWn0xpCrg)


### Downsides to shared keys and how to fix it:
#### Cons:
- Can be cracked
- Can get lost
- Can be stolen
- Needs to be transmitted

#### Fixes:
- Create long keys to slow cracking of the key

### Downsides of algorithms and how to fix it:
#### Cons:
- They always give the same output meaning easy to work out how it works and easy to backtrack to the plain text from the cipher text.

#### Fix:
- Add a key which makes every encryption unique.


## Asymmetric Encryption:
![diagram of Public-key cryptography showing public key and private key](https://lh3.googleusercontent.com/f2RL2RJY-2A_Cill1C9LBefdm9o7XzSE0jNkd8kzeFo2RUwA8frYZ3luidB8fnfWU9ODNSA9KnJMhGIPXL1ATx8PqriNOhZGMX3ZCCLUsGBTnpHCKoc1FjWG0Unj1JWLfXsxtbOzsla8_sAQeQ)
- Uses 2 Different keys
- One to encrypt the plaintext (Public key)
	- This is sent to anyone to encrypt data to send.
- One to decrypt the ciphertext (Private key)
	- This is kept private and used to decrypt the sent data.

### Examples:
- RSA
	- Same people created RC4
	- A bit slow but still widely used
- El-Gamal
	- More Advanced
	- Suffered from excessive complexity
- Elliptic Curve Cryptography (ECC)
	- Good for when resources are constrained

## Flaws in encryption:
- ### Password guessing:
	- Brute force
		- Methodical Process of trying every possible password combination
		- Very time consuming
		- Generally defeated by the inclusion of a 'Salt'
	- Dictionary attack
		- Makes use of word lists
			- Leaked passwords which are compiled together
			- just a list of words
		- Much quicker but needs to be tailored
		- Salting will again make it a lot harder

- ### Poor key Generation Procedures
	- WEP was cracked using this method.
	- If using the same key then capturing a lot of data encrypted with the same key it can be used to crack the encryption.

- ### Side Channel Attacks
	- Timing Attacks
		- Noticeable difference in how long the system processes correct/incorrect guesses
	- Power Monitoring
		- Noticeable difference in power consumption when guesses are incorrect vs correct.




![](https://lh5.googleusercontent.com/Yt9FrQ2BnZ45fbIpHi_XrzfN4ba0Ou85ZZb8tBkPv-v7WqoEYxauXrBQJN05YCXHTZqc1KXCzZh0bzgYFrYUgMH0SblJC_vnhur6qzSWTowi57rOtGtr0_uVQ6SzYMHJY-W30lPrBQB2PcBvDQ)


