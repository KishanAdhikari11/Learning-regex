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

