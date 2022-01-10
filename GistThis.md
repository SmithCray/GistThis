# <span style="color:orange">GistThis: Let's talk REGEX</span>

What is a regular expression?
<br>
Regular expressions often refered to as ["REGEX"](https://en.wikipedia.org/wiki/Regular_expression) are most often a sequence of characters used to define a search pattern within a body of text. Regular Expressions use a combination of <span style="color:green">**"Literal"**</span> characters as well as <span style="color:green">**"Meta"**</span> characters, these combined can be used to define highly complicated and fexible search patterns.

<br>

What is a <span style="color:green">**"Literal"**</span> character?
<br>

- The term Literal character is used to define any character that is simply searching for themselve.

<br>

What is a <span style="color:green">**"Meta"**</span> character?
<br>

- The term Meta character is used to define characters or combinations of them that can define more complicated search criteria than Literal's.
  Meta characters can do this by using specific syntax to define very specific perameters.
  <br>

<span style="color:yellow"> _**Let's get started then!**_ </span>

## Table of Contents:

#

- [Our Regex](#our-regex)
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)
- [Author](#author)

<br>

## Our Regex:

#

In this Gist we will be covering the following Regex used to verify user email, which is done by using a combination of <span style="color:green">**"Meta"**</span> characters defined above to set perameters in which the email input must meet or contain. Here is the example we will be using to explain the componants and purpose of them, in addition you can use the [Table of Contents](#table-of-contents) to move ahead to a specific section of the tutorial or search for a certain subject.

Matching an Email (regex snippet):
<br>

    ^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$

<br>

## Regex Components:

### Anchors:

#

Anchors belong to a group of Regex tokens we earlier defined as <span style="color:green">**"Meta"**</span> characters which do not match a specific character like <span style="color:green">**"Literals"**</span> do. Anchors can notify the engine where to start a string, the end of a line, or a determined location between the two. There are many anchor tokens availible including **"Boundaries"** and **"Delimiters"**, in the above snippet we can see use of **^Caret** which tells the engine where to start as well as the beginning of a string and at the end we see the **$Dollar** determining the end.

    ^ -- $

### Quantifiers:

#

Quantifiers are used to determine a specific instance of a character group, or class in a string, **{n}** is the simplest quantifier. In the above snippet we see the use of quantifiers in the form of **+Plus** which here defines the match of one or more times allowing user to input many characters.

    ([a-z0-9_\.-]+)

### Grouping Constructs:

#

Grouping Constructs are used to capture the sub-expressions within the input string, by using Group Constructs we can match sub-expressions as well. Here we see the use of **()Parentheses** to capture a group of sub-expressions.

    ([------])

### Bracket Expressions:

#

Bracket Expressions are one of two types either a _**Matching List Expression**_ or a _**Non-Matching list Expression**_ and consist of atleast one expression including ordinary characters, collating elements and or symbols, and even classes. As seen here we are using **[]brackets** with the addition of the **^Carot** earlier to match any single character.

    ^([-----]--)

### Character Classes:

#

Character Classes are used to define a group of given characters such as **A,B,C,** or used to define a range such as **a-z** as well as numbers like **0-9**. In the provided snippet above we see the use of classes to define user input by allowing letters including **"a"** through **"z"** as well as numbers **"0"** through **"9"**. In addition we use a **\Backslash** and a **"."** with a **"-"** to allow for periods and hyphens.

    a-z0-9_\.-

### The OR Operator:

#

The Or Operator is an optional token typically used with Boolean values and can return a boolean value as well, however this operator actually returns a specified operands and can be used without a Boolean value and will return in a non-boolean value. In our case the Or Operator is not used in the example Regex.

### Flags:

#

Flags are an optional token that is used to search either **"g" Global** or **"i" Ignore** by including the "g"-flag we can test against all possible matches in a string and by excluding it we can choose to only test the first possible match. These flags modify our search behavior and can add perameters such as case sensitivity. In the current axample we

### Character Escapes:

#

A Character Escapes is a regular expression that procedes a literal character, all characters between two given escapes are interpreted as literal characters. The backslash in combination with a given literal character can create a regex token with further meaning. Above we see the use of character escapes in multiple areas where **"\"Backslash** is present, by using this we can seperate expressions and include the presance of literal characters.

    ^([a-z0-9_\.-]+)------([\da-z\.-]+)-----\.([a-z\.]{2,6})$

### Author:

#

<br>
 
### <span style="color:orange">**Cray Smith**</span>

<img src="assets\p2cray.PNG" alt="Cray Smith GitHub" width="150px">

GitHub Link:
<br>
https://github.com/SmithCray

Email:
<br>
cmsmith004@gmail.com

<br>
