# Regex-Tutorial: Email 

In this guide, we will break down a specific regex pattern used to match and validate email addresses. By the end of this tutorial, you'll have a thorough understanding of each component of the regex pattern and how it contributes to the overall functionality. This tutorial is intended for web development students and anyone interested in learning more about regex patterns.

## Summary

The regex pattern we will be examining is:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

This pattern is used to verify that user input is a valid email address. It ensures that the email starts with a sequence of characters, followed by the @ symbol, a domain name, and a top-level domain (TLD) with specific constraints. Each part of this regex has a unique role in ensuring the email address is correctly formatted.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
Anchors are used to specify the position in the string where the match should occur.

* `^` asserts the position at the start of the string.
* `$` asserts the position at the end of the string.

        /^ ... $/
These anchors ensure that the entire string must match the pattern, not just a part of it.
### Quantifiers
Quantifiers specify how many instances of a character, group, or character class must be present for a match.

* `+` matches one or more of the preceding element.
* `{2,6}` matches between 2 and 6 of the preceding element.

        [a-z0-9_\.-]+
        [a-z\.]{2,6}

The `+` quantifier ensures that there is at least one character before the `@` and in the domain, while `{2,6}` ensures that the TLD (Top-Level Domain) is between 2 and 6 characters long.

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

This tutorial was created by Sam Cowman, a web development student learning and sharing knowledge on various programming topics . You can find more of my work on my GitHub profile: https://github.com/Sam-Cowman.

## Sources

