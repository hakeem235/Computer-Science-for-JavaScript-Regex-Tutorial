# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

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

### The following table provides examples of basic elements.

Components    | Example
------------- | -------------
`. `          | Matches any single character. For example, `cou.h` matches `couth`,`couch`, and `cough`.
`\` followed by a single character  | Lets special characters be used as a single character or “escaped For example, to use this character: `.` as a period precede it with a backslash: `\` Escaped characters are especially useful when describing paths. For example `\.html$` matches any string ending in .html. The following characters need to be preceded by a backslash if they are to be used without special meaning:`\ ` ` .`  ` $`  ` *`  `+`  `[ ] ` ` (   )` `|`
`$`| Matches any string where the specified pattern occurs at the end of the string. For example, `cause$` matches `cause` and `because` but not `causes`.
`^` | Matches any string where the specified pattern occurs at the beginning of the string. For example, `^couch` matches `couches` and `couch` but not `uncouch`. Use this element carefully when specifying a domain. For example, the expression `^/couch` matches /couch/index.htm, but not `www.domain.com/couch/index.htm`.
`[ ]` | Matches any single character in the range or set enclosed in the brackets. For example, `[aeiou]` matches any vowel. You can use a shorthand notation for a range of characters. For example, `[0-9]` matches any decimal digit. If the sequence is preceded by a carat: `^` it matches any single character not from the range or set. For example, `[^a-z]` matches any character that is not a letter of the alphabet.
`|` | Indicates an OR operator. For example: `couch|chair` finds `couch` or `chair`.
a regular expression in parenthesis `()` | Used for grouping expressions. The expression `(couch[0-9])|(bed[0-9])` matches `couch36A` or `full_bed33b` but not `couch`.
a single character	| Matches any string containing the single character to be matched. For example, `a` matches `cause`. You could also combine several characters together, such as `couch`.


### Anchors

### Quantifiers

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
