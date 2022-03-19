# Regex Expressions Explained: Matching a Hex Value

Today I will be discussing the regular expression: matching a hex value. Hex values are commonly used shorthand code for representing a certain color.

## Summary

Hex values have to satisfy certain conditions, they must start with an '#' symbol, the should be follow by letters and/or digits: a-f, A-F, 0-9, and lastly the hexadecimal code length should be 6 or 3, excluding the '#' symbol. We can use the regular expression, [regex = "^#([A-Fa-f0-9]{6}|[A-Fa-f0-9]{3})$";], to verify if a string is a correct hexadecimal value.

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

This particular regex uses 2 anchors `^` and `$`. The `^` character denotes the beginning of a string, thus the `^#` at the beginning of our expression means that it must start with a '#'.

The `$` in our expression denotes the end of a string, thus the `$` is at the end of our expression after the letter and number definitions meaning it will end in a value either a-f, A-F, or 0-9.

### Quantifiers

Quantifiers used:
`{n}`

This expression uses this quantifier appended to a character class to specify how many we need. 

In our example it comes after the same set of characters, "[A-Fa-f0-9]" twice. The first `{6}` means we need to have 6 characters. Doing so a second time with `{3}` means we can either have 6 or 3 characters. 

### OR Operator

This expression has an OR operator `|`. This means that we have multiple groups or expressions and will allow our regex to validate either set of conditions. 

### Character Classes

Character classes are enclosed in brackets. Our character class is as follows `[A-Fa-f0-9]`.  We have to repeat this class twice with an OR operator in between to say that we have two sets of conditions that can be met in order to be valid.

### Grouping and Capturing

Grouping in this expression is everything in between the (). You have two sets of the same character classes each with a quantifier. and then after you have our ending anchor. Here it is in our expression `([A-Fa-f0-9]{6}|[A-Fa-f0-9]{3})`.
### Bracket Expressions

`[A-Fa-f0-9]` iss our bracket expression. This is used to set an aray of values to look for followed by a quantifier. In this case we are looking for the characters A-F(Uppercase), a-f(lowercase), and the numbers 0-9. We have two sets of the same expression because of the quantifiers in our regex explained above.

### Greedy and Lazy Match

A greedy means match the longest possible string, while a lazy means match the shortest possible string. This can be affected by the type of quantifier used. We used `$` so we are looking for a greedy match.

## Author

My name is Christopher Pierce and I am a student in the Ohio State University Coding Bootcamp. After completion of the course I am going to start a new career in web development. Here is a link to my Github: https://github.com/christophertravisp91


