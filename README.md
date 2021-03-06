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

- [Anchors](#Anchors)
- [Quantifiers](#Quantifiers)
- [OR Operator](#OR-Operator)
- [Character Classes](#Character-Classes)
- [Flags](#Flags)
- [Grouping and Capturing](#Grouping-and-Capturing)
- [Bracket Expressions](#Bracket-Expressions)
- [Greedy and Lazy Match](#Greedy-and-Lazy-Match)
- [Boundaries](#Boundaries)
- [Back-references](#Back-References)
- [Look-ahead and Look-behind](#Look-ahead-and-Look-behind)

## Regex Components

### Anchors
Anchor is a group of components that is used to match the position of string. Components below are some examples of anchor.
```
"^" : Matches the beginning of a string. For example, "^dog" matches a string begins with "dog".
"$" : Matches the end of a string. For example, "dog$" matches a string ends with "dog". 
``` 

### Quantifiers
Quantifiers is a group of components that indicate numbers of characters or expressions to match. Components below are some examples of quantifiers
```
"*" : Matches the preceding item 0 or more times. For example, "x*" matches a string that repeats "x" 0 or more times. (it can be "" or "xxxxxxxxxxxxx")
"+" : Matches the preceding item 1 or more times.
```

### OR Operator
OR Operator "|" indicate the logical "or". For example, "dog|cat" matches "dog" or "cat". 

### Character Classes
Character classes is a group of components that distinguish type of characters. Components below are examples of Character classes.
```
"\d" : Matches any digit(0 to 9). For example "\d\d" matches any two digit numbers.
"\s" : Matches a single white space character, including space, tab, form feed, line feed, and other Unicode spaces. 
```

### Flags
Regular expressions have optional flags that allow for functionality like global searching and case-insensitive searching. These flags can be used separately or together in any order, and are included as part of the regular expression. Components below are some examples of flag.
```
"i" : Case-insensitive search
"m" : Multi-line search
```

### Grouping and Capturing
Grouping and Capturing indicate groups and ranges of expression characters. Components below are some examples of grouping
```
"()" : Matches any character inside of "()". For example "(ab)+" means any words repeating "ab", such as "ab", "ababab". 
```

### Bracket Expressions
Bracket expression "[]", match a specific set of single characters, and may match a specific set of multi-character collating elements, based on the non-empty set of list expressions contained in the bracket expression.

### Greedy and Lazy Match
Greedy and Lazy match is methods to search keywords with Regex. Greedy Match is keep searching until condition is not satisfied. Lazy Match is stop searching once condition is satisfied.

### Boundaries
Boundaries ,"\b", is a component that is a type of anchors. It matches at a position that is called a ???word boundary???. 

### Back-references
Back-references match the same text as previously matched by a capturing group. 

### Look-ahead and Look-behind
Look-ahead "(?=)" asserts that what immediately follows the current position in the string after "?=". For example, "(?=foo)" asserts that what immediately follows the current position in the string is "foo".

Look-behind "(?<=)" asserts that what immediately precedes the current position in the string after "?=". For example, "(?<=foo)" asserts that what immediately precedes the current position in the string is "foo".

## Author
This article is finished By Taeyong Lee(https://github.com/d104601)