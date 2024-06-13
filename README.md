# The Regular Expression

Regular expressions are versatile tools for pattern matching in strings. Widely used in programming languages and text editors, they facilitate tasks such as search, replace, and validation. In this example, we will discuss the regualr expression example: /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/. Throughout this assignment I will break the regex down to its simplest components and explain each part.

## Summary

In this document I will explain the regular expression, /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/. This will begin as a borad overview but will begin to focus in on each section as the document progresses. This specific regex can be used to check email addessresses for validity.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

This regex is made up on multiple individual componants, each prefoeming a different task. Like other regex's each section requires parts of the other sections to function most effectively.

### Anchors

The up carrot ( ^ ) and the dollar sign ( $ ) are anchors. Anchors signify the start and end of the regex. This is important to ensure that all componants of the regex are defined and read by the application.

### Quantifiers

Quantifiers are quite simple, they simply instruct how many times a specific set of characters should appear. In the above exmaple, the plus ( + ) quantifier explains that the element it is behing should be included at least one time. In the example the { 2, 6 } tells the regex that the character shoudl appear 2 or more times, but no more than 6 times.

### Character Classes

CHaracter classes are also quite simple, they simply define a set of characters. In this example the [a-z0-9_.-] means that all lowercase letters, all numerals, and special characters such as hyphes, underscores, and periods can be included.

### Grouping and Capturing

Parentheses (...) are used for grouping and capturing subpatterns. Our regex includes three groups to capture different parts of an email address: the username, the domain name, and the top-level domain.

1. **([a-z0-9_.-]+)**: This is the first capturing group, which matches and captures the username part of the email address. The character class [a-z0-9_.-] includes lowercase letters, digits, underscores, hyphens, and periods. The + quantifier allows for one or more occurrences of these characters.

2. **([\da-z.-]+)**: This is the second capturing group, which matches and captures the domain name part of the email address. The character class [\da-z.-] includes digits, lowercase letters, hyphens, and periods. The + quantifier allows for one or more occurrences of these characters.

3. **([a-z.]{2,6})**: This is the third capturing group, which matches and captures the top-level domain part of the email address. The character class [a-z.] includes lowercase letters and periods. The {2,6} quantifier specifies that the top-level domain should be between 2 and 6 characters long.

### Bracket Expressions

Bracket expressions ( [...] ) work alongside the characters to define specific sets of usable characters. The above regex uses brackets to match specified characters and numbers.

### Greedy and Lazy Match

Greedy match means that the regex will try its hardest to match the best possible. Lazy matching is not used by thi regex but if it were it would, only match the smallest possible similarities.

## Author

The author of this document is Nick Sprague. Nick is a graduate of Indiana University with a Masters of Science in Criminal Justice and Public Safety Management, and is a graduate student at the University of Texas at Austin's full-stack development bootcamp. Nick can be reached here: https://nicksprague1342.github.io/Portfolio/