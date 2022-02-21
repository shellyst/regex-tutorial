# Matching An Email - Regex Tutorial

This tutorial's purpose is to explain the use of regex, looking at the expression `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. This expression is used in applications requiring validation of emails, such as with MongoDB.

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors

Anchors don't match any characters at all, but are instead intended to identify the start and end of a regular expression string. In Regex, `^` is the symbol that indicates the beginning of the string. Similarily, `$` is the symbol that indicates the end of the string.

### Quantifiers

Quantifiers specify how many times a particular character, group, or character class is expected to appear within a regex string. The regex string for verifying an email contains two quantifiers, `+` and `{2,6}`. The `+` quantifier means at least one characters must appear. The `{2,6}` quantifier is read as `{min, max}`. In this case, {2,6} matches a string that has certain characters followed by 2 up to 6 characters in the preceding sequence.

### Character Classes

Character classes are notations that match any symbol from a certain set. `/d` is the digit class, with characters from 0-9. This is the character class that is used in the email matching expression. This is looking for any single character from 0-9 within our expression.

### Grouping and Capturing

Capturing groups are patters enclosed in parentheses `(...)`. Regular expressions may have multiple capturing groups. In the case of our email matching regex string, there are three capturing groups. The three capture groups are `([a-z0-9_\.-]+)`, `([\da-z\.-]+)`, and `([a-z\.]{2,6})`.

### Bracket Expressions

A bracket expression is either a matching or non-matching list expression. The contain onr more expressions from the following: ordinary characters (`A, a, or 0` for example), collating elements/symbols (any single character or sequence that collates as a single unit), character classes or range expressions.

In the matching email regex string, an example of a bracket expression is `[a-z0-9_\.-]`. Within the `[]` are the characters that the expression is looking for. In the case of this string, the characters can be `a-z` which is any letter between a and z, `0-9` which is any number between 0 and 9, `_` which looks for the literal _ character, `\.` which is a character escape, and is used following the literal use of a special character (_ in this case), and `-` which is another literal character. These make up the body of the user's email.

### Greedy and Lazy Match

## Michelle Stone

Michelle Stone is a full-stack web developer located in Ontario, Canada. Check out her work here: https://github.com/shellyst
