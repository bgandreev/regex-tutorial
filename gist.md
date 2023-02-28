# Regex Tutorial
Regular expressions, or regex, are a powerful tool for searching and manipulating text. They are used in a variety of programming languages and provide specific instructions that help computers identify patterns in text strings. In this tutorial, we will explore regular expressions and their usage.

## Summary
In specific, this tutorial will focus on the Regex seen below which is used to match valid hexadecimal color codes in CSS. Let's break down each component individually and explain what it does. 

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

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
Regular expressions are composed of several components that work together to achieve various tasks. Some examples of these components include \ . $ * ? + [ ] ( ) |, each representing a distinct element that guides the functioning of the regular expression. Let's dive deeper into these components to better understand how they operate.

### Anchors
Anchors in regular expressions are used to identify a specific position within the text, either before or after certain characters. They do not match any characters themselves, but rather make assertions about the text surrounding them. Common examples of anchors include ^ and $. The ^ anchor matches the beginning of the text, while the $ anchor matches the end of the text. In the example given, the ^ anchor is being used to search for the beginning of a line that starts with the character #. This would match any line that starts with a hashtag, such as in CSS Hex color codes for example. 

### Quantifiers
Quantifiers are elements in regular expressions that allow you to match a certain number of occurrences of a preceding character or group. In this case, the ? quantifier used in the example makes the preceding # character optional. This means that the regular expression ^#? is looking for a line that starts with a # character, but it may or may not be present in the line that matches the pattern. In simpler terms, the regular expression is looking for lines that start with a # character, but it will also match lines that do not start with # because the # character is optional. By using quantifiers in your regular expressions, you can make your searches more flexible and able to match a wider range of patterns in the text.

### Grouping Constructs
Grouping constructs in regular expressions allow you to treat multiple characters as a single unit. To create a group, simply place the characters to be grouped inside a set of parentheses, (). In the given example, the grouping construct is being used to group the characters "a-f" and "0-9" together. Specifically, the regular expression ^#?([a-f0-9]{6}|[a-f0-9]{3}) is looking for a line that starts with an optional # character, followed by a group that can contain either six or three characters that are either lowercase letters a to f, digits 0 to 9, or a combination of both.

### Bracket Expressions
The Bracket expression identifies a particular sequence of characters within square brackets, []. The given expression, "^#?([a-f0-9]{6}|[a-f0-9]{3})", specifies that the characters must be in the range of a to f or 0 to 9. To clarify, the example regular expression matches either a six-digit or a three-digit alphanumeric code preceded by an optional hash symbol. The alphanumeric characters can only be in the range of a to f or 0 to 9.

### Character Classes
A character class, also referred to as a character set, instructs a regular expression to match only one of several specified characters. The use of a hyphen inside the character class indicates a range of characters to match. In the given regular expression, the specific character classes are [a-f] and [0-9]. 

### The OR Operator
The OR operator, represented by the vertical bar symbol |, functions as a logical operator that allows for either one of two expressions to be used. In the given example, the OR operator is used between the two character classes. This indicates that either of the two expressions can be used for a match.

### Flags
Regular expressions provide optional flags that expand their capabilities to perform tasks such as case-insensitive searching and global searching. There are seven available flags:

d: This flag creates indices for substring matches.
g: This flag allows global searching which will match all occurrences in the input string.
i: This flag enables case-insensitive searching, which means the expression matches regardless of the case of the characters.
m: This flag enables multi-line searching, which matches at the beginning and end of each line in the input string.
s: This flag enables the dot (.) to match newline characters.
u: This flag treats the pattern as a sequence of Unicode code points.
y: This flag allows for a "sticky" search that starts matching at the current position in the target string.

By adding these flags to the end of a regular expression, the search can be modified to suit different requirements.

### Character Escapes
A character escape in a regular expression allows a specific character to be matched by preceding it with a backslash character. This signals to the regex engine that the following character should be treated literally, rather than as a special character with its usual meaning. In our example of the hex value, there are no escaped characters present.

