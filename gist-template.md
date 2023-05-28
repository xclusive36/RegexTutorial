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
- [More Information](#more-information)

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

The OR operator is used to match a single regular expression out of several possible regular expressions. It matches the expression before or after the OR operator. The OR operator in the string above is '|'.

```
(dogs|penguins) are cool
```

### Character Classes

Character classes match any one of a set of characters. They are also called character sets. Character classes are enclosed in square brackets []. They match any single character in that list.

```
[abc] matches a, b, or c
```

### Flags

Flags in regex expressions are optional parameters that specify the search to be global, case-insensitive, etc. Flags are placed at the end of the regex expression. For example, the 'g' flag enables global search. The 'i' flag enables case-insensitive search. The 'm' flag enables multi-line search. The 'y' flag enables sticky search. The 'u' flag enables unicode search. The 's' flag enables "dotall" search.

How do you set flags in a regex expression? Add a forward slash (/) after the closing bracket of the regex expression. Then add the flag(s) you want to use. For example,

```
/regex expression/gi.
```

### Grouping and Capturing

Grouping and capturing allows you to match a pattern multiple times, you must group using parentheses (). This allows you to apply a quantifier to the entire group or to restrict alternation to part of the regular expression. To capture the contents of a group, you can use a backreference. The captured value is stored in a backreference, which can be used later in the expression. A backreference is specified in the regex expression as a backslash (\) followed by a number indicating the number of the capturing group to be recalled.

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

### Bracket Expressions

Brackets indicate a set of characters to match. Bracket expressions are a list of characters enclosed by a pair of square brackets []. It matches any single character in that list.

If the first character after the opening bracket is a caret (^), then it matches any character not in the list.

### Greedy and Lazy Match

Greedy and lazy quantifiers match regular expressions in different ways. Greedy match is the default. It matches the longest possible part of a string that fits and returns it as a match. Lazy match finds the smallest possible part of the string and returns it as a match.

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

### Boundaries

A word boundry \b is a test just like ^ and $. It matches positions between characters. Usually a string.

There are three different positions that qualify as word boundaries: At the start of the string, if the first character is a word character. At the end of the string, if the last character is a word character. Between two characters in the string, where one is a word character and the other is not a word character.

### Back-references

A backreference is specified in the regex expression as a backslash (\) followed by a number indicating the number of the capturing group to be recalled.

### Look-ahead and Look-behind

Look-ahead and look-behind, collectively called "lookaround", are zero-length assertions. The difference is that lookaround actually matches characters, but then gives up the match, returning only the result: match or no match. That is why they are called "assertions". They only assert whether a match is possible or not.

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

## Author

- [GitHub Profile](https://github.com/xclusive36/Profile)  
- [GitHub](https://github.com/xclusive36)  
My name is Joshua Cavell. Thank you for reading my tutorial. I hope you found it helpful.

## More Information

[Regular expression](https://en.wikipedia.org/wiki/Regular_expression)  
[Regular expressions cheetsheet](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_expressions/Cheatsheet)  
[Google search](https://www.google.com/search?q=regex+expressions)