# Regex Tutorial: Matching an Email with Regex

A regular expression, regex, is a sequence of characters used to match patterns in the text. Using regex are particularly useful for extracting data like emails, phone numbers because  they follow a specific pattern from the text. They can specifically be used in any programming language like JavaScript. 

## Summary
We are here to take a in depth look into regular expressions, or regex. We first need to know what a regex is. A regex is a set of characters that defines a search pattern within a text. This is very helpful and can be used to find such items as emails, usernames, hex values, URL's, and HTML tags. Here we are going to talk about a specific example to match emails, how it breaks down into each of its components, and explains what each component does.


```
Matching an Email: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

A regular expression, is an example of a literal expression, this expression is wrapped in forward slashes (/) at the beginning and at the end of the expression. With these forward slashes, you will find the components of the regex: anchors, bracket expressions, character classes, grouping constructs, quantifiers, or character escapes, flags, and operators. 




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
Following the first forward slash you will find the circumflex  ```^``` and a dollar sign ```$``` proceeding the last forward slash. Both of these symbols are both anchors, this also is the beginning and the end of the expression. The circumflex ```^``` is the start of the string. The dollar sign ```$``` is the end of the sting. 

### Quantifiers
After the anchors in this expression, now we can see the next regex the quantifiers, a range of numbers placed between two curly brackets ```{ }``` this sets the minimum and maximum limits for each section of the string. ```{2, 6}``` is placed just to the left of the ```$``` showing the end of the expression. This quantifier says that each section of the string needs to be a minimum of 2 characters long and maximum of 6 characters. 

### Grouping Constructs
In this regex, ```()``` parentheses are used to capture a group. The first set of ```()``` captures the username of the email address, the second set captures the domain name, and the final set captures the domain. Broken down, ```/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/``` means one or more characters ```a-z``` (case insensitive), ```0-9```, ```_```, ```.```, or ```-```, followed by a literal ```@```, followed by one or more characters of any digit ```0-9```, ```a-z``` (case insensitive), ```.```, or ```-```, followed by a literal ```.```, followed by 2-6 characters ```a-z``` (case insensivite) or ```.```. Within each group construct, you can see a set of characters within brackets ```[]```, which we will talk about in the next section. 

### Bracket Expressions
The 'Bracket Expressions' ```[]``` is really anything found insides of the brackets ```[]```. Anything found inside the brackets creates a range of characters that tells us what we want to match within the text. In the expression above we can find three bracket expressions: ```[0-9]```, ```[a-z]```, and ```[_\.-]```. 

The expression ```[0-9]``` means that any number between 0 and 9. ```[a-z]``` marks any lowercase letter from a to z. Lastly, ```[_\.-] ```denotes the special characters that can be used: underscore ```(_)```, backwards slash ```(/)```, period ```(.)```, and dash ```(-)```.

### Character Classes
A character class is a set of characters that can occur in input stings to fulfill a match. The bracket expressions mentioned above are and example of this. There are two more examples that can be found in our email example from above. 

A period ```[.]``` matches any character except the newline character ```[\n]```.

```[\d]``` Matches any Arabic numeral digit. The class is equivalent to the bracket expression ```[0-9]```.

```[\w]``` Matches any alphanumeric character from the basi Latin alphabet, including the underscore ```(_)```. This class is equivalent to the bracket expression ```[A-Za-z0-9_]```.

```[\s]``` Matches a single whitespace character, including tabs and line breaks.  



### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
