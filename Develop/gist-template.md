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
- [Backreferencing](#backreferencing)
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

The code above also has a {N} quantifier, which is what is known as an interval quantifier. When appended after a character or character class it specifies how many characters are required.

### Grouping Constructs

It was previously mentioned how parentheses can be used to limit alternation, but if you also want to use a quantifier such as + or \* on more than one character at a time, then they can be grouped together using parentheses before appending a quantifier.

In the code above this grouping construct has not been used.

### Bracket Expressions

Curly brackets/ braces {} in RegEx are a quantifier that specifies the number of times a character preceding it can appear in the text or string. They can also specify a range, such as the number of times a character can appear.

Square brackets (bracket expression) is a RegEx that matches a specific set of characters and can match a set of of multi character collating elements, which are based on a set of listed expressions within the square brackets.

Parentheses () allow the user to read which characters were matched and is also useful for 'OR |" expressions.

All 3 types of brackets have been used in the credit card code mentioned above. The culry brackets have been used to determine how many times a number can appear in the text or string and the range. The square brackets show the possible match options for the numbers, alongside the range. The parentheses show which characters were matched.

### Character Classes

Character class is denoted by th euse of square brackets [] and is used to match several charcters in a particular position. The square brackets then have the characters you want matched listed inside them.

In this code the numbers [0-9] are used to offer a possible match.

The use of - bewteen the numbers is the range, so in the case of this code it is a range of 0 to 9.

### Alternation

Alternation can be used to match a single expression out of serveral regular ones.

The pipe symbol or 'OR' '|', is used to seperate options. However, this can be extended or expanded upon i.e. 1| 2| 3|.

Alternation has the lowest precedence of all RegEx operators, as it tells the engine to match everything to eithe rthe left or the right of the pipe symbol. Using parantheses within the grouping will limit its reach.

In the code above we can see the credit card code split in to serveral 'OR' sections ready for comparison.

### The OR Operator

Alternation can also be used to specify options. With alternation the pipe symbol | can be used to match subexpressions. Using | combines subexpressions, which are then called alternatives. The pipe symbol | also means 'or' so it can match various options.

Through using | in the code above it allows the numbers in the code to be matched in various ways. Also, by using parentheses the reach of the alternation can be limited.

### Backreferencing

Backreferencing also allows new patterns to be matched that are the same as a previous one. Parentheses can also be used in backreferencing, as it can remeber previously matched subexpressions.

As there can be more than one captured group, a number is used to identify the parentheses i.e. \1. You start counting the parentheses from the left. In the code above the backreferencing is shown in the last section.

### Flags

Flags are optional parameters which modify the searching behaviour of RegEx. Flags change the default search behaviour of the RegEx and makes it search differently.

Flags/ Modifiers enable the use of advanced search features, such as case insensitive or global searching. They can be used collectively or individually.

Flags were not used in the code snippet above.

### Character Escapes

Characters in RegEx that have a special meaning, require an escape sequence prefix with a backslash e.g. (\+)

Escape characters can be either inside or outside character class and have different rules depending on its location.

1. [ Escaped outside the character class
2. ] Close a character class
3. \ Used inside and outside the character class, so it must always be escaped when it specifies a literal character.
4. - Specifies character ranges inside a character class.
5. ^ This needs to be escaped outside of a character class, as it anchors the ReGex.
6. - Needs to be escaped as it is a zero or more quantifier.
7. - Needs to be escaped as it is a one or more quantifier.
8. ? Needs to be escaped as it is a zero or more quantifier.
9. { Needs to be escaped since it represents the start of a range quantifier.
10. } This character sometimes needs to be escaped as it represents the end of a range quantifier.

All of these escape characters appear in the code above.

## Author

Charlie Nunn

https://github.com/CharlieDoll/Challenge17
