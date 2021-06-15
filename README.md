# Regular Expressions

The so-called Perl compatible regular expressions offer enhancement to the POSIX-extended variety used in other software programs.
A regular expression is a string representing a pattern used for matching some portion(s) of a target string. Regular expressions are very general and as a consequence, very complex with many different types of operations represented as special characters, or meta-characters.

Regular expression syntax is usually described in a grammatical form, but we'll describe it more loosely from bottom up, the way you would created one. At the bottom are the basic components, called atoms.

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

These are special sequences which match an empty substring:
 * `^` matches at the beginning of the target string
 * `$` matches at the end of the target string
 * `\b` matches on a word `boundary`, i.e., the previous or subsequent character is not a word character

### Quantifiers

Regular expressions use quantifiers to generate unbounded matching possibilities and other matching amount specifications. An atom can optionally be followed by one of these quantifiers:
 * `*`   representing `0` or more occurrences of the atom,
 * `+`  representing `1` or more occurrence of the atom,
 * `?`  representing `0` or `1` occurrences of the atom,
* the bound `{n}`   representing exactly n occurrences of the atom,
* the bound `{m,n}`   representing between m and n occurrences of the atom. The quantifier can optionally be followed by `?` indicating that the match be minimal `(non-greedy, reluctant)` as opposed to the default maximal `(greedy)` match.

### Grouping Constructs

### Bracket Expressions

A bracket expression represents a character set via a list of characters enclosed by the square brackets: `[' and ']`. It normally matches the target string with any single character from the list.
If the character list begins with `^`, it matches any single character not from the rest of the list.

If two characters in the list are separated by `–` , this is shorthand for the (inclusive) range of characters between those two. It is illegal for two ranges to share an endpoint, e.g. a-c-e. Ranges are collating-sequence dependent and should be avoided for portability.
Most special characters lose their special status and become literals within brackets. Additionally,
* `–` is literal at the end or beginning of a bracket expression
* `^` is literal if not at the beginning of a bracket expression
The backslash character,
* ` \`, retains its meaning in bracket expressions, permitting the usage of the special escape sequences: such as `\n`, `\t`, `\w`, `\d`, etc.

### Character Classes

### The OR Operator

### Flags

### Character Escapes

These are special sequences representing commonly used character sets:
* `\w` is word (program identifier) character: `[A-Za-z0-9_]`
* `\W` is non-word character: `[^A-Za-z0-9_]`
* `\s` is a whitespace character: `[ \f\n\r\t]`
* `\S `is a non-whitespace character: `[^ \f\n\r\t]`
* `\d` is a digit character: `[0-9]`
* `\D` is a non-digit character: `[^0-9]`

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
