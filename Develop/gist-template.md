# Regular Expression - Matching a URL
This gist will explain, using Javascript, the components of a regular expression and how to use those componets to match a URL.


## Summary
Below is the regular expression of a search for user input data to validate a URL:

````
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
````
## Table of Contents

- [Regular Expression - Matching a URL](#regular-expression---matching-a-url)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
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
  - [Author](#author)

## Regex Components

### Anchors
There are two different types of anchors in a regular expression: ^ and $. When using ^, we are looking at the string that follows it and making sure it matches. In our case with validating a URL, we use the following: /^(https?:\/\/). We want the string to match "http" or "https". The ? means that the character(s) that precede it is optional. It is not neccessary to type in the "http(s)://" to direct yourself to a website.
### Quantifiers

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions
When using bracket expressions we are using, you guessed it, brackets to idenity what characters we want to match. There are multiple ways to identify specific characters in our expression. In our example, our first bracket expression is [\da-z\.-]. Using \d matches any number 0-9, while a-z matches any lowercase letter between a & z.
### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
