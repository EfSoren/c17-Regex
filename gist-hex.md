# Hex Value Regex Documentation

## Summary
In this document I will be explaining the makeup and features of a regex that can be used to find hex values. </br>
The expression we will be covering is as follows: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

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
/ - These are wrapped around the regex to enclose the expression

^ - The carrot is used to begin an instance of a string saying that it will start here

? - The question mark is a quantifier used to search for either 0 or 1 instance.

() - Parenthesis are grouping constructs used to hold the makeup of the string we will be searching for

[] - Square brackets are used to indicate bracket expressions. They will be used to hold the values our string could contain </br>
In this expression our brackets contain the following code `[a-f0-9]`

| - This is the OR operator. It is used to allow a regex to find different possible solutions.

{} - Curly Brackets are a quantifier and in this instance are used to detemine the length of the string we will be searching for

$ - The $ sign is used to depict the end of the string to be searched
### Anchors
There are two anchors used in this expression, the ^ symbol and the $ symbol.

The ^ signifies the start of the string we will be looking for and the requirements will come after.

The $ signifies the end of the string we will be searching for

### Quantifiers
Quantifiers are used as restrictions or particular rules that the expression must follow.

The ? is used to require 0 or 1 instance.
Used here `^#?`, says that the string must start with either 0 or 1 use of a # sign. </br>
This is a fancy way of saying that the string might start with a # and it might not.

There are two other quantifiers used in the expression that are set to determine the strings length.</br>
`a-f0-9]{6}` | `[a-f0-9]{3}`</br>
The {6} and {3} are saying that a string can be made of these characters and be exactly 6 characters or exactly 3 characters long.

### Grouping Constructs
We only have one set of grouping constructs in this regex. `([a-f0-9]{6}|[a-f0-9]{3})`. </br> 
This group is holding the values that regex will look for as well as any quantifiers applied to them.
### Bracket Expressions
The following bracket expression `[a-f0-9]` is used to restrict the results of the search to only return an instance of a letter a-f, or a number 0-9.</br>
That is why we apply the quantifiers {6} and {3} to filter out potential matches we dont want
### Character Classes
The character classes used in this expression are a-f and 0-9 allowing only for characters between the specified points.

### The OR Operator
The OR operator is used in this regex to allow for two different plausible returns to be found.</br
`[a-f0-9]{6}|[a-f0-9]{3}` says to find a string either 6 characters long OR 3 characters long. </br>
This is used to find hex code that might be written in different formats.

### Flags
There are no flags used in this expression but there is a flag that COULD be used.</br>
If you changed the code to include an i after the ending / it would make the search case-insensitive.</br>
This would allow results such as #ff0000 as well as #FF0000 which might be lost otherwise.

### Character Escapes
There are no character escapes used in this regex snippet

## Author
My Name is Ethan Sorensen, I am 23 years old and currently am enrolled in the University of Utah coding bootcamp.</br>
Im hoping to improve myself and learn new skills to allow me to find a career in the web development industry.</br>
Please look at my GitHub to see my other work - https://github.com/EfSoren
