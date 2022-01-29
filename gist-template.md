# RegEx Tutoral

Regex, or Regular Expression Syntax, is a useful tool for any web developer. Regular Expressions define a search pattern and are very useful for form input validation, web scraping, and filtering information. Regex may appear intimidating initially, but they can be broken down into smaller components so they can be more easily understood.

## Summary

Perhaps regex's greatest use case is in form/data validation. For instance, the following regular expression can be used to verify that user input is a valid email address:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

**Note:** Each component of this regex has a unique responsibility to make sure that a user enters an email address that begins with an unspecified number of characters preceding the `@` symbol, followed by a domain.

In this gist, the individual components of that compose a regex will be explained.

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
An *Anchor* symbolized as ^ (beginning anchor) or $ (closing anchor) signifies a string that starts with characters following it.

### Quantifiers
Quantifiers define the length of the string that your regex will match. They regularly include minimum and maximum number of characters that your regex expects.
```
{2,3} will match 2 to 3.
```

### Grouping Constructs
As patterns within a string search begin to get more complicated, *Grouping Constructs* becomes essential to partition regex using ( ) in order to match only a portion of the string at a time. Each section enclosed by parentheses is referred to as a subexpression.
```
Using the example regular expression for email validation.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

First group ([a-z0-9_\.-]+) 
Second group ([\da-z\.-]+)
Third gorup ([a-z\.]{2,6})
```
### Bracket Expressions
Anything enclosed in square brackets [] represents a set of characters we want to match. These expressions can be written to include all of the characters we want to match. For example, [abc] will look for a string that contains a, b, or c, regardless of its length.

```
[a-z0-9_\.-] it will match lower case and numbers with some special characters.
```
### Character Classes
This expression has 3 different character classes:

- ```\d``` matches with any number character ```0-9```
- ```\w``` matches any alphanumeric character including the underscore: ```a-z```, ```A-Z```, ```0-9```, and ```_```.
- ```a-z``` matches with any lowercase alphabetic character

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
