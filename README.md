# Regular Expression
In this article I will explain what is the regular expression, show examples of regular expression, and explain components of regular expression.

## Summary
Regular expression (aka regex) is a sequence of characters to search specific pattern in string. Usually, Regex is used for searching some pattern of string such as email address or URL, or replacing some pattern of string, such as changing part of SSN from number to "*".

Regex to detect social security number:
```
\d\d\d-\d\d-\d\d\d\d
```

Regex to detect Email address:
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

Regex to detect password with 1 uppercase letter, 1 number, and be at least 8 characters long: 
```
/(?=(.*[0-9]))((?=.*[A-Za-z0-9])(?=.*[A-Z])(?=.*[a-z]))^.{8,}$/
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

### Anchors
Anchor is a group of components that is used to match the position of string. Components below are common examples of anchor.
```
"^" : Matches the beginning of a string. For example, "^dog" means a string begins with "dog".
"$" : Matches the end of a string. For example, "dog$" means a string ends with "dog". 
``` 

### Quantifiers
Quantifiers is a group of components that indicate numbers of characters or expressions to match. Components below are common examples of quantifiers
```
"*" : Matches the preceding item 0 or more times. For example, "x*" means a string that repeats "x" 0 or more times. (it can be "" or "xxxxxxxxxxxxx")
"+" : Matches the preceding item 1 or more times.
```

### OR Operator
OR Operator "|" indicate the logical "or". For example "I have a (dog|cat)" means "I have a dog" or "I have a cat". 

### Character Classes
Character classes is a group of components that distinguish type of characters. Components below are common examples of Character classes.
```
"\d" : Matches any digit(0 to 9). For example "\d\d" means any two digit numbers.
"\s" : Matches a single white space character, including space, tab, form feed, line feed, and other Unicode spaces. 
```

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries
Boundaries "\b" is a component that is a type of anchors. 

### Back-references

### Look-ahead and Look-behind

## Author
This article is finished By Taeyong Lee(https://github.com/d104601)