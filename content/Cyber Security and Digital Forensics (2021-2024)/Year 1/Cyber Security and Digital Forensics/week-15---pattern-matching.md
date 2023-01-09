---
title: Week 15 - Pattern Matching
description: ""
date: 2023-01-08T23:01:39.700Z
preview: ""
draft: false
tags: ""
categories: ""
weight: 1
lastmod: 2023-01-09T00:17:27.884Z
---
# Pattern Matching

## Regular Expressions
### Keyword search:

will only match the given value not any other (e.g. matt but not mat or mathew)



### Metacharacters:

	. = any one character, except new line
	[a-z] = Any one of the enclosed characters
	* = Zero or more of proceeding characters
	? = Zero or one of the preceding character
	+ = one or more of the preceding character
	^ = Beginning of line
	$ = End of line
	\char = Escape meaning of char following it
	[^] = One character not in the set
	
	\d = Digit (0-9)
	\D = Not a Digit (0-9)
	\w = Word Character (a-z,A-Z,0-9,_)
	\W = Not a Word Character
	\s = Whitespace (Space, Tab, New Line)
	\S = Not Whitespace
	\b = Word Boundary
	\B = Not a Word Boundary

#### Shorthand Classes:

	[:alnum:] = Any Alphanumeric character
	[:alpha:] = Any Alphabetic character
	[:lower:] = Any Lowercase Character
	[:upper:] = Any Uppercase Character
	[:digit:] = Any Digits
	[:space:] = Any Spaces


##### Examples:

	[A-H] = [ABCDEFGH]
	[A-Z] = Any Uppercase Alphabetic
	[0-9] = Any Digit
	[[a] = [ or a
	[0-9\-] = Any digit or hyphen
	[^AB] = Any Character except A or B
	[A-Za-z] = Any Alphabetic
	[^0-9] = Any Character except a digit
	[]a] = ] or a
	[^\^] = Anything except ^


#### Operators:

	Sequence = None
	Alternation = |
	Repetition = \{m,n\}
	Group = (...)
	Save = \(...\)

##### Sequence Examples:

	dog = matches the pattern "dog"
	a..b = matches "a",any two characters, and "b"
	[2-4][0-9] = Matches a number between 20 and 49
	[0-9][0-9] = Matches any two digits
	^$ = Matches a blank line
	^.$ = Matches a one-character line
	[0-9]-[0-9] = Matches two digites seperated by a "-"

##### Alternation Examples:

	UNIX|unix = Matches "UNIX" or "unix"
	Ms|Miss|Mrs = Matches "Ms" or "Miss" or "Mrs"

##### Repetition Examples:

Formats:
	
	{m} = Matches previous atom exactly m times
	{m, } = Matches previous atom m times or more
	{ ,n} = Matches previous atom n times or less
	{m,n} = Matches previous atom m times to n times
	
Examples:
	
	CA{5} = Matches "CAAAAA"
	CA{3,} = Matches "CAAA", "CAAAA", "CAAAAA", ...
	CA{,2} = Matches "C", "CA", or "CAA"
	A{3,5} = Matches "AAA","AAAA", or "AAAAA"
	BA{3,6} = Matches "BAAA","BAAAA","BAAAAA", or "BAAAAAA"

###### Short Form Repetition Operators:

Formats:
	
	* = Special case: Matches previous atom zero or more times
	+ = Special case: Matches previous atome one or more times
	? = Special case: Matches previous atom 0 or one time only 
		
Examples:
	
	BA* = Matches "B", "BA", "BAA", "BAAA", "BAAAA", ...
	B.* = Matches "B","BA" ... "BZ","BAA" ... "BZZ","BAAA" ... "BZZZ", ...
	.* = Zero or more characters
	.+ = One or more characters
	[0-9]? = Zero or one digit
	
##### Group Operator Examples:
	A(BC){3} = Matches "ABCBCBC"
	(F(BC){2}G){2} = Matches "FBCBCGFBCBCG"


