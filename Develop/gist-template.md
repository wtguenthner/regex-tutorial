# Regular Expression Tutorial - Matching a URL
This gist will explain, using Javascript, the components of a regular expression and how to use those components to match a URL.


## Summary
Regex allows us to verify a search by using specific sequences of characters. In our example, we are using the following expression to validate a URL.

````
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
````
Using this expression we are using regex components to verify each portion of a users input to make sure it is a valid URL. Below we will explain each component being used and how that is checking the user's input to validate a response.

## Table of Contents

- [Regular Expression Tutorial - Matching a URL](#regular-expression-tutorial---matching-a-url)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [Character Classes](#character-classes)
    - [Grouping and Capturing](#grouping-and-capturing)
    - [Bracket Expressions](#bracket-expressions)
    - [OR Operator](#or-operator)
    - [Greedy and Lazy Match](#greedy-and-lazy-match)
  - [Author](#author)

## Regex Components

### Anchors
There are two different types of anchors in a regular expression: `^ and $`. When using `^`, we are looking at the string that follows it and making sure it matches. In our case with validating a URL, we use the following: `/^(https?:\/\/)`. We want the string to match `http` or `https`. The `?` means that the character(s) that precede can be matched zero or one time. It is not neccessary to type in the `http(s)://` to direct yourself to a website.

### Quantifiers
Quantifiers are used to select a specific amount of characters in a string or a section. There are a few different ways to apply this component. In this portion of the expression, `([a-z\.]{2,6})`, the curly brackets are our quantifier. When using the curly brackets we are telling the expression to match the previous string `[a-z\.]` a minimum of 2 times but a maximum of 6 times. Note that because we are using `a-z` it is checking for any lower case letters. For example, "COdE" would not match because it only contains one lower case letter. Using this expression with only one number inside of the curly brackets means the pattern must be matched for the exact number inside the brackets.


### Character Classes
The character class component is used to define a specific set of characters that will validate the expression. We use a few different character classes in our example. The first is `\d` which matches any digit `0-9`. Another that we use is `\w` which matches any upper or lower case letter, any number, as well as an underscore. We are also using `.` in our expression which matches any character with the exception of the newline character. A newline character signifies the end of a line of text and the start of a new one.

### Grouping and Capturing
Grouping allows use to section off portions of the expression for validation. The way that we group these portions is by using parenthesis. Because there are multiple portions to examine with different requirements to match we must use grouping. Below are a few examples from our above expression:
  - `(https?:\/\/)?`
  - `([a-z\.]{2,6})`
  - `([\/\w \.-]*)` 

### Bracket Expressions
When making a bracket expression we are using, you guessed it, brackets to idenity what characters we want to match. There are multiple ways to identify specific characters in our expression. In our example, our first bracket expression is `[\da-z\.-]`. Using `\d` matches any number `0-9`, while `a-z` matches any lowercase letter between a & z.

### OR Operator
While using bracket expression, we are allowing multiple options to establish validity. In this portion of our expression: `[\da-z\.-]` we are checking for any digit OR any letter `a-z`. The OR operator is the `|` symbol so our expression could also be written as `[\d|a-z]` and it would serve the same function.

### Greedy and Lazy Match
When using quantifiers we are applying one of two types of matches: greedy or lazy. By default quantifiers are greedy, meaning that are trying to match the given pattern as much as possible. You can change a quantifier to be lazy be adding a `?` after which will match the pattern the fewest amount possible.

## Author

This tutorial was created by Taylor Guenthner. [Github Profile](https://github.com/wtguenthner)
