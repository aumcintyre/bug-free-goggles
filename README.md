# Email Verification With a Regular Expression (REGEX)

In this tutorial, I will be explaining how to match text strings to a regular expression, ensuring that the string is correctly formatted as an acceptable email address. 

## Summary

- RegEx being used: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

    >* The above expression will be used to verify that a user-input string is correctly formatted as an email address. Below I will break down each portion of this expression.
## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

# Regex Components

## Anchors

The anchors for any regex are simply the characters that indicate where the expression begins and where it ends. In the case of our email-matching regex, we will use `^` to begin our expression, and will use `$` to end the expression. Some expressions will allow the use of `(m)` for a multi-line regex, but that is not the case here. 

## Quantifiers
In this regex, we are using 2 different quantifiers. These quantifiers ensure that the preceeding block of characters matches our pattern a set number of times.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

- In our regex above, we are using 2 different quantifiers

    >* `+`   is used to ensure that the first and second portion of the email address are at least 1 character long, but aren't limited to a maximum amount of characters
    >* `{2,6}`   is the other quantifier that we are using, and that is ensuring that the final portion of the email address is between 2 and 6 characters, and that each character matches what we allow in our pattern.

## OR Operator

This regex does not use an OR Operator.

## Character Classes

Regex: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

 - In this particular expression, we are using 5 different character classes.
    >* `/d`  -- This character class will match any SINGLE digit character from 0 to 9. This may also include any Unicode character that has a digit attribute.
    >* `0-9`  -- Similar to `/d`, but this is strictly matching characters from 0-9.
    >* `a-z` -- This class will match any letter from a to z, as long as that letter is lowercase.
    >* `/.`  -- This is how we match a period. Since it has a special use in regex, so we use the slash preceeding it to escape its typical useage.
    >* `@` -- This simply matches the @ symbol, where it should be used in an email address.


## Flags

This regex currently uses no flags. With regular expressions, there are a total of six (6) optional flags. The `g` flag is one that is often used with an email regex, and it requires that the regular expression is tested against all possible matches in the string. Without the `g` flag, like in our example, it will test it only for the first class that the string matches.

## Grouping and Capturing

- This expression looks for three (3) capturing groups. 
    >* `([a-z0-9_\.-]+)` : This is matching the user's email name. It is looking for a string containing lowercase a-z, digits 0-9, an underscore, a period, or a hyphen. If the string contains anything else, this verification will fail.
    >* `([\da-z\.-]+)` : This group is looking for a string containing the email domain or service. It is expecting to receive only digits 0-9, lowercase letters a-z, a period, or a hypen. Again, if the regex receives anything other than these characters, the verification will fail. 
    >* `([a-z\.]{2,6})` : The third group is looking for the final portion of the email address after the period. This is typically com, net, org etc. The regex is expecting to receive only lowercase letters or a period, and the string should be between 2 and 6 characters long. 


## Bracket Expressions

The bracket expressions in a REGEX are there to contain all the character classing within a certain grouping. Again, we use three (3) in this REGEX

- Bracket Expressions
    >* `[a-z0-9_\.-]`
    >* `[\da-z\.-]`
    >* `[a-z\.]`

## Greedy and Lazy Match

Greedy and lazy match quantifiers are used in regular expressions to indicate how many times the string should match the expression. In this email regex, we are using 2 greedy quantifiers and 0 lazy.

- Greedy Quantifiers
    >* `+` ; The plus sign quantifier requires that at at least ONE character be included that matches the expression, but it will check as many times as possible against all included characters.
    >* `{ 2, 6 }` The curly brackets allow the regex creator to set an exact amount, or a minimum and a maximum amount of characters. In this example, this grouping must have at least 2 characters, but no more than 6.

- Lazy Quantifiers
    >* None

# Author

The author of this REGEX is Austin McIntyre. You can find more of my projects on my GitHub here: www.github.com/aumcintyre
