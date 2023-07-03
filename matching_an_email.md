# Regex Tutorial: Matching an Email

This Tutorial will explain the use of regex or regular expression for matching an email. Regex is sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input.

## Summary

In order to match an email, the Regex will look like the following code:

```/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/```

This is used to validate if the input email matches an email address.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors

There are two anchors in this regex ```^``` and ```$```.

```^``` Indicates the beginning of the string

```$``` Indicates the ending of the string

### Quantifiers

There are two quantifiers in ths regex. the first is ```+```, this matches one or more of the preceding token. In this regex the emai name matches any of the characters ```[a-z0-9_\.-]``` and the email service matches any of the characters ```[\da-z\.-]```. Any capital letters or characters outsided of the specifically listed groups would not match.

This regex also uses the quantifier ```{2,6}``` which is used after the character class ```[a-z\.]``` in the capturing group ```([a-z\.]{2,6})```. This group matches a sequence of ```2``` to ```6``` lowercase letters or dots. This means the email address must end with a two to six lettertop level domain, like .com, .edu, or .gov.

### Character Classes

The character class in this expression is ```\d```, which matches a single character that is a digit from 0-9. It will only match a single digit such as ```8```, but not ```888```.

### Flags

### Grouping and Capturing

Capturing group #1 in this expression is ```([a-z0-9_\.-]+)``` that matches the user email name. The second capturing group is ```([\da-z\.-]+)``` which will match the email service. Then the third capture group #3 is ```([a-z\.]{2,6})``` to capture the .com.

### Bracket Expressions

Bracked expressios for email validation includes the character sets of ```[a-z0-9_\.-]```, which is matching any letter a-z and is case senstive. It also matches a character 0-9 and matches the characters "_" , "-" , and "."; ```[\da-z\.-]```, which is matching a single digit from 0-9, any character a-z (case senstive), and the characters "." and "-".; ```[a-z\.]``` matches any character a-z(case senstive) and the character ".".

### Greedy and Lazy Match

This regrex includes greedy matches. Since it includes the ```+``` Quantifier, it will match as many times as possible giving back as needed. Another greedy Quantifier used in this regex is ```{}``` when matching ```{2,6}``` for the last capture group.

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

This regex tutorial was created by Jerrick Johnson

Github Profile: https://github.com/JerrickJohnson