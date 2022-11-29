# Regex tutorial: Email validation
Regular expressions use characters to locate specific patterns in text. Recognizing and validating an email address or finding the specific text patterns in a URL. These methods can be used in search and replace operations. They are commonly used in search engins and text editors. 


## Summary
The validation of an emails address is important for a large multitude of reasons. Making sure the correct information is placed within the text box and to make sure the emails entered has no typoes. These typos can be detremental. If for example a user is able to create an emails with characters like #$% these could be consiedred invalid operatores and the email might not work on other websites. Having a regex validation in place makes sure that whoever is creating the email makes one that will work on other websites. As a side not email validation is almost always used on the front end.


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
All of the different components that create a specific regex are different. Different characters have different meanings and the formulation of those characters in the regex can find or ignore different pattern. All rgular expressions are made up of different components. A common email validating regex is as follows: /^[a-zA-Z0-9.!#$%&'*+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:\[a-zA-z0-9-]+)*$/. This looks through the email that is asking for validation and depending on the want of the code matches the patterns and constrains to either validate or throw out the email. 

### Anchors
Anchors are the start and finish of a regular expression they themselvs do not validate individual matching characters but they are used to match the begining and ends of the provided string. Below are the characters normally used to get this informaiton:

This: ^ matches the information at the begining of the line

This: $ matvhes the informaiton at the end of the line

### Quantifiers
Quantifiers set bounderies on how many instences of characters, groups or classes must be in the given input for a match and validation to be found. In this example of email validation: 
/[w._%+-]+@[\w.-]+\.[a-zA-Z]{3,6} 
we see the use of the + this can be used to set the number of times the input should match in this case it is set to match as many times as possible. The ? can be used as a logical yes or no setting the regex to search the input zero or one time.

### Grouping Constructs
Grouping Constructs can be used to breakdown and match the small strings in an input string. "In this small string" Grouping Constructs don't come into play much. For example if we want our regex to find all instences do the letter "s" capitalized or not we can easily do that. "However, in this second string of larger and more complicated characters we can use Grouping Constructs to find much more." If we wanted to find all of the words that has 2 letters our regex might have trouble doing that as the words to,of and in are all different but they fit that criteria.

### Bracket Expressions
Bracket expressions are used to set search parameters within the regex. For example: [a-zA-Z] is an expression that says "search all lowercase letters a-z then search all uppercase letters A-Z. These can be used in a variaty of ways to specifically find validation within the regual expressions. Another expression of this is the number of matches {2,5} this asks fo match at least 2 times but no more then 5. Bracket expressions can be great ways of specifying bounteries and connecting several of them together can be done with quantifiers as can be see in the regex example from the regex components section and ion the example in the quantifiers section.

### Character Classes
Character Classes are related to bracket expressions in they are the instructions contained with in the brackets. Character Classes can be used to find broud ranges of information to specific characters sopmetimes only one character and soemtimes many. Example of Character Classes can be as follows: [abc] this Character Classe find the letters a, b and c in a regex. [^abc] this Character Classe find all characters except those listed within the brackets. The example used in the bracket expressions find all characters from a-z and A-Z. 

While these are all great the question of how to deal with rnges comes to mind. For example if I want to find most of the alpabet in my input string except for for a a couple characters rather then typing out all but those characters I can use validators like this: [a-z &&[^gt]] this finds all characters within the input string from a-z except for the characters g and t. If i want a larger range I can use [a-z &&[^d-s]] this subtracts all letters from d-s. The only letters used in searching the given string are those that are not between d-s. 

### The OR Operator
The OR Operator is represented as |. In english it can be similar to and/or. In the previous examples we looked at the difference between a-z and A-Z. However, wd can simplify that and turn it into something like a-z|Z. This looks for all characters from a-z or Z. Simplifying the need for more then one rulling for capitalization and lowercase.

### Flags
Like in javascript Flags can be used to set global limiatations or clarification for the expression. However, unlike in javascript they are always at the end of the regex and always in lowercase. Here are some examples of flags and what they are capable of: s: This represwents Dot All. This matches all wild characters to newlines. m: This represents Multiline this keeps and organizes the anchor properties. i: this represents Ignores casing. Making the regex case-sensitive. These are some fo the most popular flags used in regular expressions.

### Character Escapes
Character Escapes are methods used to well escape characters. They have different applications but they can be used to extract words or phrases dirrectally from the given input. If my name Bjorn was used I could escape that word using an expression like (\w+). If the sectence was "Bjorn who will you decide to be?" If I wanted to escape my own anme and the question mark I could add .+ to my regex after the escape to make (\w+).+ this should give the output of Bjorn? for the example sentince.  

## Author
My name is Bjorn Addington. I am an aspiring developer currentally taking a full stack bootcamp at the university of WA. I am excited to start my career in tech!

Authors GitHub: https://github.com/Franswarduvar
Authors LinkedIn: https://www.linkedin.com/in/bjorn-addington-3083a2239/
