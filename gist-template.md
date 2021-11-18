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

Grouping constructs are what allows the quantifiers to match a specific section of the regex and allows the retrieval and separation of different subexpressions.  A subexpression is any valid regular expression pattern and is denoted with parenthesis -(subexpression).  The email matching regex has three separate subexpressions.  Each one is used to perform different matching methods.

### Bracket Expressions
A bracket expression is denoted just as the name sounds, within brackets.  This tells the engine to match any character within the brackets.  The email matching regex has three bracket expressions within each of the three grouping constructs.  The parameters for the matching are outside of the brackets but within the grouping constructs.  That is because it is structured like the following: 

            anchor([characters to be matched]how the characters should be matched)

### Character Classes
Character classes define how the characters should be included (i.e. uppercase, lowercase, punctuation characters, ect).  The character classes are defined within the bracket expressions.  In the email matching regex, the first grouping construct is the following -([a-z0-9_\.-]+). The character classes shown within the bracket expression have a range of lowercase letters (a-z), a range of numbers (0-9), and the use of the following symbols _\.- that must be included at least once due to the "+" at the end of the bracket expression.
### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
