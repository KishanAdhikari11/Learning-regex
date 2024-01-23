# Regular Expressions (Regex) in Python

## Introduction

Regular expressions, often abbreviated as regex or regexp, are powerful tools for pattern matching and text manipulation. In Python, the `re` module provides support for regular expressions.

This README.md file serves as a beginner-friendly guide to understanding and using regular expressions in Python.

## Table of Contents

1. [Getting Started](#getting-started)
   - [Installation](#installation)
   - [Importing the `re` Module](#importing-the-re-module)
2. [Basic Patterns](#basic-patterns)
   - [Literal Characters](#literal-characters)
   - [Character Classes](#character-classes)
   - [Quantifiers](#quantifiers)
3. [Special Characters](#special-characters)
   - [Anchors](#anchors)
   - [Wildcard](#wildcard)
   - [Escaping Special Characters](#escaping-special-characters)
4. [Groups and Capturing](#groups-and-capturing)
   - [Capturing Groups](#capturing-groups)
   - [Non-Capturing Groups](#non-capturing-groups)
5. [Advanced Patterns](#advanced-patterns)
   - [Lookahead and Lookbehind](#lookahead-and-lookbehind)
   - [Backreferences](#backreferences)
6. [Common Use Cases](#common-use-cases)
   - [Email Validation](#email-validation)
   - [URL Matching](#url-matching)
   - [Phone Number Matching](#phone-number-matching)


## Getting Started

### Installation

You don't need to install anything specific for regular expressions in Python, as the `re` module is part of the standard library.

### Importing the `re` Module

To use regular expressions in your Python code, you need to import the `re` module:

```python
import re
```
## Basic Patterns
### Literal Characters
A literal character or matching something literally refers to specfying an actual character in the text.
### Example
- 'a' is a literal character that matches lowercase letter 'a'.
- '123' matches exact sequence of '1','2','3' in order.

#### Code

```python
import re

# Example: Matching the literal character 'cat'
pattern = re.compile('cat')
result = pattern.search('The cat is fast')
print(result.group())  # Output: 'cat'
```
### Character Classes
The character class in regex let us define a set of characters that we want to match. It is placed inside the big bracker [].
### Example 
- [cat] matches a literal 'cat'
- [0-9]: It matches a range of number from 0 to 9.
- [^0-9]: It matches a range of number other than 0 to 9.

#### Code
```python
import re
# Example : usage of character class in regex
patern=re.compile('[0-9]')
pattern1=re.compile('[a-zA-Z0-9_]')
res=pattern1.search('Hello') #output: H
result=pattern.search('The number is 94')
print(result.group()) #output: 9
```
### Quantifiers
| Quantifier | Description                                                  | Example                           |
|------------|--------------------------------------------------------------|-----------------------------------|
| *          | Matches 0 or more occurrences of the preceding element.    | a* matches '', 'a', 'aa', 'aaa', ... |
| +          | Matches 1 or more occurrences of the preceding element.    | a+ matches 'a', 'aa', 'aaa', ... but not an empty string. |
| ?          | Matches 0 or 1 occurrence of the preceding element (makes it optional). | a? matches an empty string or 'a'. |
| {n}        | Matches exactly n occurrences of the preceding element.    | a{3} matches 'aaa'.               |
| {n,}       | Matches n or more occurrences of the preceding element.    | a{2,} matches 'aa', 'aaa', 'aaaa', ... |
| {n,m}      | Matches between n and m occurrences of the preceding element (inclusive). | a{2,4} matches 'aa', 'aaa', or 'aaaa'. |

#### Code
``` python
import re

# Example 1: Using *
pattern1 = re.compile(r'a*')  # Matches 0 or more 'a' characters
result1 = pattern1.match('aaab')
print(result1.group())  # Output: 'aaa'

# Example 2: Using +
pattern2 = re.compile(r'\d+')  # Matches 1 or more digits
result2 = pattern2.search('The number is 12345')
print(result2.group())  # Output: '12345'

# Example 3: Using ?
pattern3 = re.compile(r'colou?r')  # Matches 'color' or 'colour'
result3a = pattern3.search('The color is red')
result3b = pattern3.search('The colour is blue')
print(result3a.group())  # Output: 'color'
print(result3b.group())  # Output: 'colour'

# Example 4: Using {n}
pattern4 = re.compile(r'\d{3}')  # Matches exactly 3 digits
result4 = pattern4.search('The code is 12345')
print(result4.group())  # Output: '123'

# Example 5: Using {n,}
pattern5 = re.compile(r'a{2,}')  # Matches 2 or more 'a' characters
result5 = pattern5.search('The cat is sleeping on the mat')
print(result5.group())  # Output: 'aa'

# Example 6: Using {n,m}
pattern6 = re.compile(r'\d{2,4}')  # Matches 2 to 4 digits
result6 = pattern6.search('The year is 2022')
print(result6.group())  # Output: '2022'

```













