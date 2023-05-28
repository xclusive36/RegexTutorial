# RegexTutorial

Hello, in this tutorial I will explain how to use a Regex expression.

## Summary

Matching an Email Address with Regex you can use the following expression:

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

The first part of an email address is the username. All characters leading up to the '@'. As such, the first part of the Regex expression checks the username. It can be any combination of letters, numbers, underscores, periods, and dashes.

```
([a-z0-9_\.-]+)
```

The second part of an email address is the domain name. All characters after the '@' and before the '.'. (dot) As such, the second part of the Regex expression checks the domain name. It can be any combination of letters, numbers, underscores, periods, and dashes.

```
([\da-z\.-]+)
```

The third pard of an email address is the top-level domain. All characters after '@' and then after the '.' (dot) As such, the third part of the Regex expression checks the top-level domain. It can be any combination of letters, numbers, underscores, periods, and dashes.

```
([a-z\.]{2,6})
```

The expression will match any email address that has a username, domain name, and top-level domain.


### Anchors

Anchors are a different kind of regex token. It doesn't match any character at all. Instead, it matches a position before, after, or between characters. It asserts the engine's current position in the string. It matches a location at the beginning of the string, or the end of a line.

It lets you specify where you want to match digits, not anywhere else. It lets you find a compex pattern at a specific location.

The anchors in the string above are '^' and '$'.

'^' indicates the beginning of a string.

'$' indicates the end of a string.

### Quantifiers

Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found.

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

The quantifiers in the string above are '+' and '{2,6}'.

'+' matches the previous token between one and unlimited times, as many times as possible, giving back as needed.

'{2,6}' matches the previous token between 2 and 6 times, as many times as possible, giving back as needed.

### OR Operator

The OR operator is used to match a single regular expression out of several possible regular expressions.

### Character Classes

Character classes match any one of a set of characters. They are also called character sets.

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

[Regular expression](https://en.wikipedia.org/wiki/Regular_expression)
[Regular expressions cheetsheet](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_expressions/Cheatsheet)
[Google search](https://www.google.com/search?q=regex+expressions)