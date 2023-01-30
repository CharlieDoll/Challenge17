# Title (Regular Expressions (RegEx) and Credit Card Numbers)

Regular expressions are a useful programming tool and can help to make text programming more efficient. Using RegEx to solve problems can help to improve productivity. It can also be used to match and describe text and will also allow you to find, verify and replace text and format it.

## Summary

The code snippet below is for validating credit card numbers. They normally require a secure platform but RegEx can also be used to validate for only minimal requirements. Some credit cards require more specific codes, which can be found at the website below:

https://stackoverflow.com/questions/9315647/regex-credit-card-number-tests/23231321#23231321

RegEx Credit Card Code:
^(?:4[0-9]{12}(?:[0-9]{3})?|5[1-5][0-9]{14}|6(?:011|5[0-9][0-9])[0-9]{12}|3[47][0-9]{13}|3(?:0[0-5]|[68][0-9])[0-9]{11}|(?:2131|1800|35\d{3})\d{11})$

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Alternation](#alternation)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

Anchors are classed as MetaCharacters and examine the beginning and end of the line of text that they are examining. They state where a boundry exists, through the use of ^ and $.

In the code snippet above ^ anchors a literal to the beginning of the line and matches the start of the line.
In the code snippet above $ anchors a literal at the end of the line and matches the end of the line.

The characters ^ and $ only match the position of the characters in the credit card pattern and not the actual characters in the code.

As there are no words in the code above there are no word boundaries, so the anchors b and B are not required.

### Quantifiers

The use of quantifiers denotes how many times a character, character class or group should appear in the text.

In the code snippet above the quantifier used is ? and implies 'optional', so it states that a character may or may not appear.

The code above also has a {N} quantifier, which is what is known as an interval quantifier. When appended after to a character or character class it specifies how many characters we want.

### Grouping Constructs

### Bracket Expressions

### Character Classes

Character class is denoted by th euse of square brackets [] and is used to match several charcters in a particular position. The square brackets then have the characters you want matched listed inside them.

In this code the numbers [0-9] are used to offer a possible match.

The use of - bewteen the numbers is the range, so in the case of this code it is a range of 0 to 9.

### Alternation

Alternation can also be used to specify options. With alternation the pipe symbol | can be used to match subexpressions. Using | combines subexpressions, which are then called alternatives. The pipe symbol | also means 'or' so it can match various options.

Through using | in the code above it allows the numbers in the code to be matched in various ways. Also, by using parentheses the reach of the alternation can be limited.

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
