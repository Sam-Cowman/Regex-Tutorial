# Regex-Tutorial: Matching an Email 

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
Parentheses () are used for grouping and capturing parts of the pattern.

* `([a-z0-9_\.-]+)` captures the local part of the email.
* `([\da-z\.-]+)` captures the domain name.
* `([a-z\.]{2,6})` captures the top-level domain (TLD).

        ([a-z0-9_\.-]+)
        ([\da-z\.-]+)
        ([a-z\.]{2,6})

These groups capture different parts of the email address, which can be useful for further processing.

### Bracket Expressions
Bracket expressions, also known as character classes, define a set of characters to match.

* `[a-z0-9_\.-]` matches any lowercase letter, digit, underscore, dot, or hyphen.
* `[\da-z\.-]` matches any digit, lowercase letter, dot, or hyphen.
* `[a-z\.]` matches any lowercase letter or dot.

        [a-z0-9_\.-]
        [\da-z\.-]
        [a-z\.]

These classes ensure that only valid characters are used in the email address.

### Character Classes
Character classes define a set of characters to match. In the regex pattern for email validation, we use:

* `\d` to match any digit (equivalent to `[0-9]`).

        [\da-z\.-]

This class ensures that both digits and letters are valid characters in the domain name.

### The OR Operator
The OR operator `|` is not used in this specific regex pattern. However, it is important to note that it is used to match either the expression before or the expression after the operator.

### Flags
Flags are optional parameters that modify the behavior of the regex pattern. This pattern does not use any flags. Common flags include:

* `i` for case-insensitive matching.
* `g` for global matching.
* `m` for multi-line matching.
### Character Escapes
The `\` character is used to escape special characters in regex.

* `\.` matches a literal dot `.`.

        \.

Escaping the dot ensures that it is treated as a literal character rather than a special regex metacharacter.
## Author

This tutorial was created by Sam Cowman, a web development student learning and sharing knowledge on various programming topics . You can find more of my work on my GitHub profile: https://github.com/Sam-Cowman.

## Sources
This tutorial is based on knowledge and information gathered from the following sources:

1. MDN Web Docs - Regular Expressions:

* [MDN Web Docs: Regular Expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_expressions)

2. Regular-Expressions.info:

* [Regular Expressions Tutorial](https://www.regular-expressions.info/tutorial.html)

3. GeeksforGeeks - Regular Expressions in JavaScript:

* [GeeksforGeeks Regex in Javascript](https://www.geeksforgeeks.org/regular-expressions-in-javascript/)

4. Regex Tutorial: Matching a Username:

* [Full-Stack Coding Boot Camp: Regex Tutorial](https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial)

These sources provide comprehensive explanations and examples that helped shape this tutorial on regex patterns for email validation.
