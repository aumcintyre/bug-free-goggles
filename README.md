# Title (replace with your title)

In this tutorial, I will be explaining how to match text strings to a regular expression, ensuring that the string is correctly formatted as an acceptable email address. 

## Summary

- RegEx being used: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

    >* The above expression will be used to verify that a user-input string is correctly formatted as an email address. Below I will break down each part of this expression while also explaining their function.

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

The anchors for any regex are simply the characters that indicate where the expression begins and where it ends. In the case of our email-matching regex, we will use `^` to begin our expression, and will use `$` to end the expression. Some expressions will allow the use of `(m)` for a multi-line regex, but that is not the case here. 

### Quantifiers
In this regex, we are using 2 different quantifiers. These quantifiers ensure that the preceeding block of characters matches our pattern a set number of times.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

- In our regex above, we are using 2 different quantifiers

    >* `+`   is used to ensure that the first and second portion of the email address are at least 1 character long, but aren't limited to a maximum amount of characters
    >* `{2,6}`   is the other quantifier that we are using, and that is ensuring that the final portion of the email address is between 2 and 6 characters, and that each character matches what we allow in our pattern.

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
