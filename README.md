# Matching an Email

(example)
 `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Summary

Here we have a regex expression that allows us to check if our user inputs some text that matches a string with the correct characters for an email. Regex is an easy and simple way to make sure that our user's imputs are correct and clean so we can efficiently manage our code. 

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

* * *

## Regex Components
//
^
([a-z0-9_\.-]+)
@
([\da-z\.-]+)
\\.
([a-z\.]{2,6})
$

* * *

### Anchors

Anchors do not match any character at all. Instead, they match a position before, after, or between characters. They can be used to “anchor” the regex match at a certain position. The caret ^ matches the position before the first character in the string. 
Similarly, \$ matches right after the last character in the string. c\$ matches c in abc, while a\$ does not match at all.

* * *

### Quantifiers

A number in curly braces {n} is the simplest quantifier. When you append it to a character or character class, it specifies how many characters or character classes you want to match.
For example, the regular expression `/\d{4}/` matches a four-digit number. It is the same as `/\d\d\d\d/`
* * *

### OR Operator
The pipe or the '|' character allows for our regex extression to have an option between this OR that.
For example, supposing that '|' is the alternation operator, then `foo|bar|quux` would match any of `foo, bar or quux`.
* * *

### Character Classes

With a “character class”, also called “character set”, you can tell the regex engine to match only one out of several characters. All you need to do is place the characters you want to match between square brackets. If you want to match an a or an e, use [ae]. You could use this in gr[ae]y to match either gray or grey.
* * *

### Flags

A regular expression consists of a pattern and optional flags: g , i , m , u , s , y . Without flags and special symbols the search by a regexp is the same as a substring search. 
An example would be having a 'g' at the end of our regexp allows us to search 'globally' throughout the whole text we are testing.
* * *

### Grouping and Capturing

Parentheses group the regex between them. They capture the text matched by the regex inside them into a numbered group that can be reused with a numbered backreference. They allow you to apply regex operators to the entire grouped regex. 
An example would be `/(abc){3}/` matches abcabcabc. First group matches abc.
* * *

### Bracket Expressions
A bracket expression is a list of characters enclosed by ‘[’ and ‘]’. It matches any single character in that list. 
The sorting sequence is the native character order; for example, ‘[a-d]’ is equivalent to ‘[abcd]’.
* * *

### Greedy and Lazy Match

'Greedy' means match longest possible string.
'Lazy' means match shortest possible string.
For example, the greedy `/h.+l/` matches 'hell' in 'hello' but the lazy `/h.+?l/` matches 'hel'.
* * *

### Boundaries

The metacharacter \b is an anchor like the caret and the dollar sign. It matches at a position that is called a “word boundary”. This match is zero-length.
\b allows you to perform a “whole words only” search using a regular expression in the form of `\bword\b`. A “word character” is a character that can be used to form words. All characters that are not “word characters” are “non-word characters”.

* * *

### Back-references

Backreferences match the same text as previously matched by a capturing group.
For example, the regex `\b(\w+)\b\s+\1\b` matches repeated words, such as `regex regex`, because the parentheses in `(\w+)` capture a word to Group 1 then the back-reference \1 tells the engine to match the characters that were captured by Group 1.
* * *

### Look-ahead and Look-behind

Lookahead and lookbehind, also known as called “lookaround”, are zero-length assertions just like the start and end of line, and start and end of word anchors.
`(?=foo)`=> Lookahead
`(?<=foo)`=> Lookbehind
* * *

## Author
[Leo Ayala](https://github.com/leo-ayala)

