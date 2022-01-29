# RegEx Tutoral

#### **Note:** <a href="https://gist.github.com/OmarAce/e46792d10a337aa594a0f321fbdbc43f"> This is a link to the deployed Gist </a>

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

### **Anchors**

An *Anchor* symbolized as ^ (beginning anchor) or $ (closing anchor) signifies a string that starts with characters following it.

### **Quantifiers**

Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found.

<table width="100">
<tr>
<td align='center'> <strong>Greedy Quantifier </strong></td>
<td align='center'> <strong>Lazy Quantifier</strong> </td>
<td align='center'> <strong>Description</strong></td>
</tr>
<tr>
<td> * </td>
<td> *? </td>
<td align='center'> <em> Match zero or more times </em></td>
</tr>
<tr>
<td> + </td>
<td> +? </td>
<td align='center'> <em> Match one or more times </em></td>
</tr>
<tr>
<td> ? </td>
<td> ?? </td>
<td align='center'> <em> Match zero or one time </em></td>
</tr>
<tr>
<td> { n } </td>
<td> { n }? </td>
<td align='center'> <em> Match exactly n times </em></td>
</tr>
<tr>
<td> { n ,} </td>
<td> { n ,}? </td>
<td align='center'> <em> Match at least n times </em></td>
</tr>
<tr>
<td> { n , m } </td>
<td> { n , m }? </td>
<td align='center'> <em> Match from n to m times </em></td>
</tr>
</table>

The quantities n and m are integer constants. Ordinarily, quantifiers are greedy; they cause the regular expression engine to match as many occurrences of particular patterns as possible. Appending the ? character to a quantifier makes it lazy; it causes the regular expression engine to match as few occurrences as possible. 

### **Grouping Constructs**

As patterns within a string search begin to get more complicated, *Grouping Constructs* becomes essential to partition regex using ( ) in order to match only a portion of the string at a time. Each section enclosed by parentheses is referred to as a subexpression.
```
Using the example regular expression for email validation.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

First group ([a-z0-9_\.-]+) 
Second group ([\da-z\.-]+)
Third gorup ([a-z\.]{2,6})
```

### **Bracket Expressions**

Anything enclosed in square brackets [] represents a set of characters we want to match. These expressions can be written to include all of the characters we want to match. For example, [abc] will look for a string that contains a, b, or c, regardless of its length.

```
[a-z0-9_\.-] it will match lower case and numbers with some special characters.
```

### **Character Classes**

This expression has 3 different character classes:

- ```\d``` matches with any number character ```0-9```
- ```\w``` matches any alphanumeric character including the underscore: ```a-z```, ```A-Z```, ```0-9```, and ```_```.
- ```a-z``` matches with any lowercase alphabetic character

### **The OR Operator**
| symbolizes the OR or 'Alternate' operator which essentially performs a either match whatever's to the left or right of the '|'. 
'''
a(b|c)     matches a string that has a followed by b or c (and captures b or c)
'''
### **Flags**
A regex usually comes within this form /abc/, where the search pattern is delimited by two slash characters /. At the end we can specify a flag with these values (we can also combine them each other):
```
g—Global search: the regex should be tested against all possible string matches.

i—Case-insensitive search: When looking for a match in a string, case should be ignored.

m—Multi-line search: a multi-line input string should be interpreted as multiple lines.
```

### **Character Escapes**
Character Escapes means an escaping backslash mush be present before special function characters for the Regex to look for strings. There are two in this Regex Expression:

1. ```\/``` used to match with a forward slash ```/```
2. ```\.``` used to match with a period ```.```

### **Author**

This RegEx Tutorial was created by <a href="https://github.com/OmarAce">Omar Acevedo</a>
