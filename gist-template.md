# Email Validation with Regular Expressions Tutorial

Regular expressions (regex) are powerful tools for pattern matching and string manipulation in programming. They allow you to create complex search patterns to match specific strings, such as email addresses, phone numbers, and URLs. In this tutorial, we'll focus on using regex to validate email addresses, breaking down the pattern piece by piece to understand how it works.


## Summary

In this tutorial, we will examine a regular expression pattern used to validate email addresses. The pattern ensures that the email format is correct, including the presence of an @ symbol, a valid domain, and a top-level domain (TLD). Here's the regex we'll be exploring:

`const emailPattern = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;`

We’ll explain how the different components of this regex come together to ensure that email addresses are correctly formatted.


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
Anchors are used to match the position within a string. In our email validation regex:

- `^` ensures that the string starts with the given pattern.
- `$` ensures that the string ends with the given pattern.

This means that the entire string must match the email pattern, not just a part of it.


### Quantifiers
Quantifiers specify how many times an element in the regex should appear:

- `+` means "one or more" of the preceding character class or group.


### Grouping Constructs
Grouping allows us to treat part of a pattern as a single unit. In the email regex, there is no explicit grouping using parentheses (), but grouping can be used to create complex patterns, such as matching an entire domain as a unit.


### Bracket Expressions
Bracket expressions, or character sets, match any one of the characters inside the brackets:

- [a-zA-Z0-9._%+-] matches any alphanumeric character, periods, underscores, percentage symbols, plus signs, or hyphens.

This bracket expression ensures that only valid characters are allowed before the @ symbol.


### Character Classes
Character classes allow us to match a range of characters. In the email regex:

- [a-zA-Z] matches any uppercase or lowercase letter.`

- [0-9] matches any digit.

These classes are useful for ensuring that domain names and TLDs are composed of letters and/or numbers.


### The OR Operator
The OR operator | is used to match one pattern or another. While this regex does not use the OR operator, it is commonly used to match alternatives. For instance, you could create a regex that matches either example.com or test.com.


### Flags
Flags are optional parameters that modify the behavior of the regex. Common flags include i for case-insensitive matching and g for global matching. Our email regex does not use any flags, but you could add the i flag to ignore case differences in the email domain.


### Character Escapes
Character escapes are used to treat special characters as literal characters. For instance:

 - `\.` matches a literal dot (.) instead of the dot's special meaning (which is to match any character).

In this regex, `\.` ensures that we are matching actual periods in the domain name.


## Author

Written by Chris Robinson

[Github Link](https://github.com/crob127)