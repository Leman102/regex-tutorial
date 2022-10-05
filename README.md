# Match Email Regular Expressions Tutorial ![](https://img.shields.io/static/v1?label=Hi&message=Welcome%20to%20my%20Regex%20tutorial&color=blue)

The purpose of this gist is to explain what a Regular Expression (Regex) is and how to use it.

**When do we use Regex?**

Regex is not only used to match a specific character combination within a string but also it can be used for validation or to pull out information from a given body of code.

"_A programmer's best friends Google and Regex_".

## Summary

In this tutorial we will follow a regular expression that can be used to validate if an email follows the correct format.  

* Matching an email expression: **`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`** 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)

## Regex Components

### Anchors

Anchors are regex tokens that don't match any characters but ensures that a matched expression is anchored to a certain position in the string. 

Anchors are the caret symbol `^` which asserts that we are at the beginning of the string and the dollar sign`$` which asserts that we are at the end of the string. 

Our email Regex, is saying that we are looking for something that starts with :

`^([a-z0-9_\.-]+)` 

And it has to end with:

`.([a-z\.]{2,6})$`.

We will define what's inside of the parentheses later in this tutorial.

### Quantifiers

Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found.

If we look at our code for matching the email:

`([a-z0-9_\.-]+)` 

This will match any string that contains letters (a-z), numbers (0-9), underscores (_), dots (.) or dashes (-) and the quantifier `+` specifies that it has to contain at least one of this in order to have a match. 

### Character Classes

A character class is a special notation that matches any symbol from a certain set.

The digit class `\d` is present in the given matching email Regex and it will match a single letter character, a-z, after the `@` sign in the email address. Basically ensuring that a letter is matched after the `@` in the email and not a number or special character.  

`@([\da-z\.-]+)`
### Grouping and Capturing

Capturing groups are a way to treat multiple characters as a single unit. They are created by placing the characters to be grouped inside a set of parentheses.

In the matching email example we have three groups:
- `([a-z0-9_\.-]+)` is the first group that appears in our regex. This must be true before moving on to the next expression. 
- `([\da-z\.-]+)` is the second group, if true, moves to next group. 
- `([a-z\.]{2,6})` is the third group, if true, all the "matching an email" conditions are valid.
### Bracket Expressions

Bracket expressions can be used to match a single character or collating element.

Continuing with the Regex for matching an email:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

The snippet `[a-z0-9_\.-]` specifies that just letters a-z, numbers 0-9, an underscore, hyphen, or period are accepted. The period is an escaped character, therefore, it requires the backslash to match.
## Author

- **GitHub repository:**
  **[regex-tutorial](https://github.com/Leman102/regex-tutorial)**
- **GitHub Profile:**
  **[Leman102](https://github.com/Leman102)**
- **E-mail:**
  **leonelmancerap@gmail.com**
- **Gist:**
  **[match-email-regex-tutorial](https://gist.github.com/Leman102/3c8598030d388cb52b9e2b87e071c966)** 
