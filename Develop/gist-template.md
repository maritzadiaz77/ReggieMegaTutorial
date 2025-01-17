# myRegexTutorial

## Summary
Hello, my name is Maritza Diaz and I will be showing you my Regex Tutorial and the example we are going to be looking at is trying to match an HTML Tag. We'll be breaking it down and explaining what every piece of this regex means.
"Matching an HTML Tag - /^<([a-z]+)([^<]+)(?:>(.)</\1>|\s+/>)$/"
A regex, which stands for regular expression, is a sequence of characters that defines a search pattern in a search pattern for text.
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
-The characters ^ and $ are both considered to be anchors. -The ^ anchor signifies a string that begins with the characters that follow it. This matches a position, not a character.

-The $ anchor signifies a string that ends with the characters that precede it. Just as with the ^ character, it can be preceded by an exact string or a range of possible matches.This matches a position, not a character.

If you notice on our regex, we begin with an ^ and end with a $!
### Quantifiers
Quantifiers set the limits of the string that your regex matches (or an individual section of the string). They frequently include the minimum and maximum number of characters that your regex is looking for.

These are some quantifiers.

*—Matches the pattern zero or more times

+—Matches the pattern one or more times

?—Matches the pattern zero or one time

{}—Curly brackets can provide three different ways to set limits for a match:

{ n }—Matches the pattern exactly n number of times

{ n, }—Matches the pattern at least n number of times

{ n, x }—Matches the pattern from a minimum of n number of times to a maximum of x number of times.
### OR Operator
Using the OR operator (|), the expression [abc] could be written as (a|b|c), or a or b or c. For example: (abc):(xyz) And then use the OR operator to convert it to the following: (a|b|c):(x|y|z) Now, both of the strings "abc:xyz" and "acb:xyz" would match, as well as "a:z", but "xyz:abc" would not.

As you can see, our regex /^<([a-z]+)([^<]+)(?:>(.)</\1>|\s+/>)$/" has an or operator as well.
### Character Classes
A character class in a regex defines a set of characters, any one of which can occur in an input string to fulfill a match.

Here are some common character classes:

. Matches any character except the newline character (\n)

\d Matches any Arabic numeral digit. This class is equivalent to the bracket expression [0-9].

\w Matches any alphanumeric character from the basic Latin alphabet, including the underscore (). This class is equivalent to the bracket expression [A-Za-z0-9].

\s Matches a single whitespace character, including tabs and line breaks

Each of the last three character classes can be changed to perform an inverse match by capitalizing the letter character. For example, \D matches a non-digit character.
### Flags
Flags are placed at the end of a regex, after the second slash, and they define additional functionality for the regex. There are six optional flags that can be used, either separately or together and in any order, but these are the three you're most likely to encounter:

g—Global search: the regex should be tested against all possible matches in a string.

i—Case-insensitive search: case should be ignored while attempting a match in a string

m—Multi-line search: a multi-line input string should be treated as multiple lines
### Grouping and Capturing
(ABC)CAPTURING groups multiple tokes together and creates a CAPTURE group for extracting the substrin or using a backreference. \1 is a numeric Referance (?:ABC) Groups multiple tokens together without creating a capture group. (?< name >ABC) named capturing group captures groups of a specific name.
### Bracket Expressions
Anything inside a set of square brackets ([]) represents a range of characters that we want to match. These patterns are known as bracket expressions, but they are also known as a positive character group, because they outline the characters we want to include. We can write these expressions to include all of the characters we want to match. For example, [abc] will look for a string that includes a or b or c.

You'll more commonly see a hyphen (-) used between alphanumeric characters (letters and numbers only) to represent a range of those possible characters. This means that [a-c] and [abc] will look for the exact same thing.

[a-z]—The string can contain any lowercase letter between a–z. Keep in mind that this looks for lowercase characters only. If we wanted to include uppercase characters, we would need to change the expression to [a-zA-Z].

[0-9]—The string can contain any number between 0–9

[_-]—The string can contain an underscore or hyphen.
### Greedy and Lazy Match
Quantifiers are GREEDY, meaning they match as many occurrences of particular patterns as possible. They include the following:

*—Matches the pattern zero or more times

+—Matches the pattern one or more times

?—Matches the pattern zero or one time

{}—Curly brackets can provide three different ways to set limits for a match:

{ n }—Matches the pattern exactly n number of times

{ n, }—Matches the pattern at least n number of times

{ n, x }—Matches the pattern from a minimum of n number of times to a maximum of x number of times.

Each of these quantifiers can be made lazy by adding the ? symbol after it, meaning it will match as few occurrences as possible.
### Boundaries
Boundary markers such as ^ and $ allow you to anchor the regex pattern to the beginning and end of the line. This means that when you want to match a literal ^ or $ , you need to escape these special characters with a backslash.
### Back-references
Backreferences match the same text as previously matched by a capturing group. If you want to match a pair of opening and closing HTML tags, and the text in between. By putting the opening tag into a backreference, we can reuse the name of the tag for the closing tag.
### Look-ahead and Look-behind
(?=ABC) is a postive look-ahead and it matches a group after the main expression without including it in the result.

(?!ABC) is a negative look-ahead and it specifies a group that can not match after the main expression.

(?<=ABC>) is a postive look-behind and matches a group before the main expression without including it in the result.

(?<!ABC) is a negative look-behind and Specifies a group that can not match before the main expression.

Looka-heads and look-behinds forcesthe main expressions to be what you have defined it as. Without it being exactly what it is it will not be accepted as a valid input.
## Author
My name is Maritza Diaz and I am learning to be a full-stack dev. Here is my GitHub profile https://github.com/maritzadiaz77.
Here is my source that I referred to, which was ultimately helpful to learn. https://www.youtube.com/watch?v=7DG3kCDx53c, Google, and https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial/ .