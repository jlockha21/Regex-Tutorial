# RegEx Tutorial

In this session, we will explore a practical example of a regular expression, commonly known as a regex.

## Summary

Essentially, a regex is a combination of characters that defines a specific pattern search within a given text. It's highly useful in various contexts, such as identifying usernames, email addresses, hexadecimal values, URLs, and HTML tags. In this article, we present an example of an email validation pattern below. We will break down this regex, examine its individual components, and explain their respective functionalities.

Email Validation Pattern: /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/

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

### Anchors

Following the first forward slash, you will find the symbol (^), denoting the start, and a dollar sign ($), indicating the end of the expression. These symbols function as anchors, marking the respective boundaries of the regex. The caret (^) signifies the beginning of a string, while the dollar sign ($) represents its conclusion.

### Quantifiers

After the anchors, attention is drawn to quantifiers, represented by numeric ranges enclosed in curly brackets ({}). These brackets establish minimum and maximum limits for each section of the string. In the example above, you can see the quantifier detailed in the summary.

The {2,6} sequence is positioned just before the dollar sign ($), signifying the expression's conclusion. This quantifier dictates that each string section should consist of a minimum of 2 characters and a maximum of 6 characters.

### Grouping Constructs

Regular expressions are typically partitioned using parentheses (). In this example, the groups are of the capture type, preserving matched sequences for future use. Examining the provided instance, you can observe three distinct sections: ([a-z0-9_.-]+), ([\da-z.-]+), and ([a-z.]{2,6}). Within each grouping, a set of characters is enclosed within brackets ([]).

### Bracket Expressions

A bracket expression encompasses characters enclosed within brackets ([]), forming a character range for matching within the text. In the provided example, three bracket expressions are present: [0-9], [a-z], and [_.-].

[0-9] covers numbers from 0 to 9.
[a-z] represents lowercase letters from 'a' to 'z'. For uppercase letters, [a-zA-Z] would be used.
[.-] denotes special characters: underscore (), forward slash (/), period (.), and dash (-).

### Character Classes

A character class defines a set of permissible characters within input strings for a match. The previously mentioned bracket expressions exemplify this concept. Our email example introduces two more character classes.

A period (.) matches any character except the newline character (\n).
(\d) signifies any Arabic numeral and corresponds to the bracket expression [0-9].

### The OR Operator

The "OR" operator in a regex is represented by a vertical bar (|). This operator offers alternatives during word or character searches. For instance, the regex four|for|floor|4 accepts "four," "for," "floor," or "4." While the example provided lacks an OR operator, we introduced one here to illustrate its application.

### Flags

Flags are optional parameters in a regex that modify search behavior. Six flag types exist: 'i' (Ignore Casing), 'g' (Global), 's' (Dot All), 'm' (Multiline), 'y' (Sticky), and 'u' (Unicode).

'i' makes the search case-insensitive.
'g' prompts the search for all occurrences.
's' ensures the wild character '.' matches newlines.
'm' makes '^' and '$' match line beginnings and endings.
'y' starts searching from the indicated index.
'u' handles Unicode.

### Character Escapes

The final component of interest is character escapes. These employ a backslash to indicate the character following it for regex interpretation, rather than treating it literally. In our example above, you'll encounter one such instance: (.). This signals the regex to directly interpret a period (.) instead of employing the character class's use of the same symbol.

## Author

This learning experience has been profoundly humbling for me. While not devoid of challenges, exploring new realms of knowledge has proven incredibly fulfilling. The satisfaction of completing projects and assignments has made the journey worthwhile.

GitHub: https://github.com/liljlock
