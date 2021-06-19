# Regex Hex code verification tutorial

In this tutorial we will be going over a short demonstration and explanation of regular expressions (regex).

## Summary

Regex allows you to search a string of text for certain information that you want based on the regex that you choose.  
An example of this is:
```
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/
```
This is a regular expression used to verify the given string is in the proper format for a 3/6 digit hex code.  
We will go over all of the components used for this below.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)

## Regex Components

### Anchors
The ^ anchor is used to check the beginning of a string:
```
^# will check for the character "#" at the start of a string.  
"#5 is my favorite number" will pass.
```

the $ anchor is used to check the end of a string:
```
j$ will check if the given string ends with a 'j'.  
"My least favorite letter is j" will pass.
```

### Quantifiers
The ? quantifier will check for exactly one or zero instances of the character/string:
```
#? will check to see if there is either one or zero '#' in the string.  
Both "#5 is my favorite number" and "5 is my favorite number" will pass.
```

The {} quantifier will check for however many instances of a character/string as the number inside the squigly brackets:
```
#{5} will check to see if there are five instances of the '#' character.  
"##### is too many pounds signs" will pass.
```

### OR Operator
The or operator can be used to check for one of several different options:
```
(a|b) will check for either 'a' or 'b' in the given string.  
Both "I like a nice slice of pizza" and "I like b nice slice of pizza" will both pass.
```

### Grouping and Capturing
In order to group certain pieces of a regex you need to include them in '()':
```
(abc)? will check for one or zero "abc" strings.  
Note that it is checking for all three letters and not just the one before ?.  
"The first three letters of the alphabet are abc" will pass.
```

### Bracket Expressions
Bracket expressions are used to match one of the characters on the inside of the bracket:
```
[a-f0-9]? will check for one or zero instances of any characters between a-f or 0-9.  
Both "b is my favorite letter" and "6 is my favorite number" will pass.
```

## Author

My name is john haller and i am the author [Github](https://github.com/HallerJohn)
