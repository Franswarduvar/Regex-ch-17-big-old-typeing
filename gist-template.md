# Title 
Regex write up!
## Summary

Bracket expressions allow for the matching of information. Here is an example: [nN] [oO] these can be sorted into four pairs no, nO, No and NO. Another example is as follows: gr[ae]y, this can be sorted into 2 possibilities gray, and grey. 

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
Any regular expression element can be qualified by one of the following three characters: *, +, or ?.
In general, regular expressions are not as resource-efficient as absolute definitions, and the more complex the regular expression, the more resources are allocated to matching. If you find that using complex regular expressions causes performance problems, keep in mind that regular expressions using beginning-of-string matching (^) and end-of-string matching ($) are the most efficient.
### Anchors
Anchores come as they sound, providing additional information on the regex, this enables it to understand where to start and where to end. Example of anchores include: ^ and $. 

^ forces the regex to start at the begining of the string, this can return valuses that are at the begining of the given information but are not towards the end.
'$' forces the string to start from the back this will return iunformation starting at the back of the string. For example with the string 'cat' both ^ and $ return a true value however, with the word wildcat only $ returns true.

Other anchors include =, ., \
### Quantifiers
Quantifiers give and validate the number of instances an expression is allowed to return. A list of quantifiers goes as follows: *, +, ?, { n }, { n ,}, { n , m } they can be describes as follows:

*'        Matches zero or more times.
+'        Matches one or more times.
? 	      Matches zero or one time.
{ n }     Matches exactly n times.
{ n ,}    Matches at least n times.
{ n , m } Matches from n to m times.
There are also things called Lazy quantifiers which are slight modifications of the quantifiers that change the number of times.
### Grouping Constructs
Grouping constructs delineate the subexpressions of a regular expression and capture the substrings of an input string. You can use grouping constructs to do the following:

Match a subexpression that is repeated in the input string.

Apply a quantifier to a subexpression that has multiple regular expression language elements. For more information about quantifiers, see Quantifiers.

Include a subexpression in the string that is returned by the Regex.Replace and Match.Result methods.

Retrieve individual subexpressions from the Match.Groups property and process them separately from the matched text as a whole.
### Bracket Expressions
A bracket expression (an expression enclosed in square brackets, "[]" ) is an RE that shall match a specific set of single characters, and may match a specific set of multi-character collating elements, based on the non-empty set of list expressions contained in the bracket expression.
### Character Classes
In the context of regular expressions, a character class is a set of characters enclosed within square brackets. It specifies the characters that will successfully match a single character from a given input string.
### The OR Operator
I was unable to find anything about this in regards to regex expressions
### Flags
The "g" after the regular expression is an option or flag that performs a global search, looking in the whole string and returning all matches. It is explained in detail below in Advanced Searching With Flags.
Regular expressions have optional flags that allow for functionality like global searching and case-insensitive searching. These flags can be used separately or together in any order, and are included as part of the regular expression.
### Character Escapes
Let’s say we want to find literally a dot. Not “any character”, but just a dot.

To use a special character as a regular one, prepend it with a backslash: \..

That’s also called “escaping a character”.
## Author

My name is Bjorn, I am an aspiring developer looking to do my best and start my career. Link to my GitHub profile: https://github.com/Franswarduvar
