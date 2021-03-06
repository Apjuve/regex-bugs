# Title (REGEX)

Short for regular expression, a regex is a string of text that allows you to create patterns that help match, locate, and manage text. Its useful for extracting information from a body of code. 

## Summary

Regular Expression E-mail matching example. This code will be used throughout the lesson to demostrate the usefulness of the various components of regex. 
\b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b. 

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

Anchors are a different breed. They do not match any character at all. Instead, they match a position before, after, or between characters. The anchor starts and end the regular expression. 

\b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b. 


### Quantifiers

Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found. examples,

*, *?,+, +?, ?, ??, { n }, { n }?, { n ,}, { n ,}?, { n , m }, { n , m }?

### OR Operator

Grouping and alternation are core features of every modern regular expression library. You can provide as many terms as desired, as long as they are separated with the pipe character: |. 
example;

([a-f0-8]{6}|[a-f0-8]{3})

### Character Classes

With a “character class”, also called “character set”, you can tell the regex engine to match only one out of several characters. Simply place the characters you want to match between square brackets.

example;

 [0-9a-fA-F] 


### Flags

A flag changes the default searching behaviour of a regular expression. It makes a regex search in a different way.
A flag is denoted using a single lowercase alphabetic character.
In JavaScript regex, we have a total of 6 flags, each serving a different purpose.

i - Makes the expression search case-insensitively.
g - Makes the expression search for all occurrences.
s - Makes the wild character . match newlines as well.
m - Makes the boundary characters ^ and $ match the beginning and ending of every single line instead of the beginning and ending of the whole string.
y - Makes the expression start its searching from the index indicated in its lastIndex property.
u - Makes the expression assume individual characters as code points, not code units, and thus match 32-bit characters as well.

### Grouping and Capturing

Groups use the ( ) symbols (like alternations, but the | symbol is not needed). They are useful for creating blocks of patterns, so you can apply repetitions or other modifiers to them as a whole. 
example; 

([a-x]{3}[0-9])+, the + metacharacter is applied to the whole group.

### Bracket Expressions

Brackets indicate a set of characters to match. Any individual character between the brackets will match, and you can also use a hyphen to define a set.

example;

[A-Za-z] [0-9]

'elephant'.match(/[abcd]/) // -> matches 'a'

### Greedy and Lazy Match

'Greedy' means match longest possible string.

example;

 h.+l

'Lazy' means match shortest possible string.

exmple;

h.+?l

### Boundaries

To make it easier to find whole words, we can use the metacharacter \b. It marks the beginning and the end of an alphanumeric sequence*.

example;

\bstack\b	foo stack bar

### Back-references

Backreferences match the same text as previously matched by a capturing group.

example;

<([A-Z][A-Z0-9]*)\b[^>]*>.*?</\1>. 

This regex contains only one pair of parentheses, which capture the string matched by [A-Z][A-Z0-9]*

### Look-ahead and Look-behind
Lookahead and lookbehind, collectively called “lookaround”, are zero-length assertions just like the start and end of line, and start and end of word anchors.
The difference is that lookaround actually matches characters, but then gives up the match, returning only the result: match or no match. That is why they are called “assertions”. They do not consume characters in the string, but only assert whether a match is possible or not.

## Author

Tutorial was created by Abi Ponce

[GitHub] (https://github.com/Apjuve)
[Email] (abiponce.ap@gmail.com)