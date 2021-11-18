# Regex Tutorial - Matching an Email

Regular expressions can be used to verify many different strings and are especially useful when building a user login function. 
## Summary

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

The symbols, numbers, and letters above are a part of a regular expression.  These expressions are used to match character combinations in strings.  The specific one above takes emails and matches them to verify if it is authentic or invalid.  The following tutorial will explain in detail the functionality of the email regex and break down the expression into a way that is easier to understand each section.

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
An anchor is used to assert a position in the string for the matching process.  It tells the search engine that the following characters are the ones that you want to use in the matching process and saves the engine time trying to look through the code for it.  The anchor is show by the carrot symbol "^" and in this case, it is placed at the beginning of the regex right after the forward slash.  The anchor at the end of the regex is the "$" symbol.  This allows the engine to easily go through the matching process along the line of code and understand the beginning and the end of the email being matched.
### Quantifiers
Quantifiers are used to specify how many of each character needs to be included in the email.  The quantifiers can be a variation of the following characters: "*", "+", "?", and {n}.  The first three characters listed tell the engine that they need to match a character anywhere between zero or more / zero to one times.  It basically just says whether or not the character should be included or not included.  To make a specific character quantity match, the {n} must be used where the "n" would show a specific number for how many times you want the character to be included.

In the email match regex, `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`, you can see that the "+" and the "{n}" were used to quantify the required characters.  The {2,6} says that the character must match from 2 to 6 times, and the "+" must match one or more times - which just is saying it has to be included at least once.
### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)