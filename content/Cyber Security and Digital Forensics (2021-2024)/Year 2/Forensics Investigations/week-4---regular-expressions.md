---
title: Week 4 - Regular Expressions
description: ""
date: 2023-05-19T02:56:19.816Z
preview: ""
draft: false
tags: ""
categories: ""
weight: 0
---
## Why regular expressions?
- Regex
- Allows searching using a range of characters rather than just the keyword
- More Powerful than keyword search

## Regex:
- A Pattern of special characters used to match strings in a search
- Typically made up from special characters called meta-characters
- Used throughout the web, software and Linux
	- grep, egrep, sed, and awk
	- Python

### Meta-characters:
- `.` - Will match any character except a new line character
- `[-]` - Will match one character from a range of characters on its left and right
- `*` - Will match zero or more of the preceding character
- `?` - Will match zero or one of the preceding characters
- `+` - Will match one or more of the preceding characters
- `^` - Beginning of the line
- `$` - End of the line
- `\char` - Escape the meaning of the *char* following it
- `[^]` - One of the character not in the set
- `\b`  - Beginning/End of the word anchor
- `|`  - OR grouping
- `x{m}` - Repetition of the character *x*, *m* times
- `x{m,}` - Repetition of the character *x*, at least *m* times
- `x{m,n}`  -Repetition of the character *x* between *m* and *n* times
e.g. 
```r
[A-H] -> [ABCDEFGH]
[A-Z] -> Any Uppercase alphabetic
[0-9] -> Any digit
[[a] -> [ or a
[0-9\-] -> Any Digit or hyphen
[^AB] -> Any character except A or B
[A-Za-z] -> Any alphabetic
[^0-9] -> Any character except a digit
[]a] -> ] or a
[^/^] -> Anything except ^
```

### Anchors:
Anchors tell where the next character in the pattern must be located in the text data.
- `^` - Beginning of line
- `$` - End of line
- `\b` - Beginning of word
- `\b` - End of word
- `\A` - Beginning of string
- `\z` - Very end of string
- `\Z` - End of string (or before optional line break)
- `\G` - Beginning of string or end of previous match

#### e.g.
`[a-zA-Z0-9_]` - are word characters
`\b4\b` - will match 4 but not 44
`\bis\b` - will match **is** in the string "This island is beautiful." but nothing else

### Back References:
We can use back references in regex to re-use previously matched patterns in the regex
- The pattern is defined by brackets `(regex)`, and then the matched text can be recalled from a buffer using: `\<buffer-number>`
- `buffer-number` increments with each back reference

`([a-c])x\1x\1` - Matches **a**xaxa , **b**xbxb and **c**xcxcx where the reference is in bold

### Alternation / OR operator: |
The operator `|` is used to match one **or** more alternatives.
- `UNIX|unix` → matches "UNIX" or "unix"
- `Ms|Miss|Mrs` → matches "Ms" or "Miss" or "Mrs"
- `cat|dog|mouse|fish`  → matches those words

### Repetition Operator: {…}
The repetition operator specifies that the expression immediately before the repetition may be repeated.
- `A{3,5}` → matches "AAA", "AAAA", or "AAAAA"
- `BA{3,5}` → matches "BAAA", "BAAAA", or "BAAAAA"

#### Basic repetition forms:
- `{m}` - matches previous atom exactly *m* times
- `{m,}` - matches previous atom *m* or more times
- `{,n}` - matches previous atom *n* times or less
#### e.g.
```r
CA{5} -> CAAAAA
CA{3,} -> CAAA, CAAAA ,CAAAAA , ...
CA{,2} -> C, CA, CAA
```

### Group Operator:
In the group operator, when a group of characters is enclosed in parentheses the next operator applies to the whole group, not only the previous characters.
#### e.g.
```r
A(BC){3} -> ABCBCBC
(F(BC){2}G){2} -> FBCBCGFBCBCG
```