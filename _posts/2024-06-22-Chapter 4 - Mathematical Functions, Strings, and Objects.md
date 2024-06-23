---
layout: post
title: Chapter 04 - Mathematical Functions, Strings, and Objects
categories: [COSC1436]
tags: [notes, python]
---

### Contents

1. [Common Python Functions](#common-python-functions)
2. [Strings and Characters](#strings-and-characters)
4. [The 'ord' and 'chr' Functions](#the-ord-and-chr-functions)
5. [Escape Sequences for Special Characters](#escape-sequences-for-special-characters)
6. [Printing without the Newline](#printing-without-the-newline)
7. [The 'str' Function](#the-str-function)
8. [Concatenation and Repetition Operators](#concatenation-and-repetition-operators)
9. [Reading Strings from Console](#reading-strings-from-console)
10. [The 'in' and 'not in' Operators](#the-in-and-not-in-operators)
11. [Comparing Strings](#comparing-strings)
12. [Functions for Strings](#functions-for-strings)
13. [Index Operators '[ ]'](#index-operators)
14. [The Slicing Operator '[start:end]'](#the-slicing-operator-startend)
15. [Introduction to Objects and Methods](#introduction-to-objects-and-methods)
16. [String Methods](#string-methods)

## Common Python Functions

>*Python provides many useful functions for common programming tasks.*

### Simple Python Built-in Functions

| Function       | Description                                                                                 | Example                 |
|----------------|---------------------------------------------------------------------------------------------|-------------------------|
| **abs(x)**         | Returns the absolute value for x.                                                           | `abs(-2)` is `2`        |
| **max(x1, x2, ...)** | Returns the largest among x1, x2, ...                                                       | `max(1, 5, 2)` is `5`   |
| **min(x1, x2, ...)** | Returns the smallest among x1, x2, ...                                                      | `min(1, 5, 2)` is `1`   |
| **pow(a, b)**      | Returns a^b. Same as a ** b.                                                                 | `pow(2, 3)` is `8`      |
| **round(x)**       | Returns an integer nearest to x. If x is equally close to two integers, the even one is returned. | `round(5.4)` is `5`  |
|                |                                                                                             | `round(5.5)` is `6`     |
|                |                                                                                             | `round(4.5)` is `4`     |
| **round(x, n)**    | Returns the float value rounded to n digits after the decimal point.                        | `round(5.466, 2)` is `5.47` |
|                |                                                                                             | `round(5.463)` is `5.4` |

### Mathematical Functions

The python <span class="code green">math</span> module provides these mathematical functions:

| Function       | Description                                                                                 | Example                 |
|----------------|---------------------------------------------------------------------------------------------|-------------------------|
| **fabs(x)**         | Returns the absolute value for x as a float.                                              | `fabs(-2)` is `2.0`     |
| **ceil(x)**         | Rounds x up to its nearest integer and returns that integer.                              | `ceil(2.1)` is `3`      |
|                |                                                                                             | `ceil(-2.1)` is `-2`    |
| **floor(x)**        | Rounds x down to its nearest integer and returns that integer.                            | `floor(2.1)` is `2`     |
|                |                                                                                             | `floor(-2.1)` is `-3`   |
| **exp(x)**          | Returns the exponential function of x (e^x).                                              | `exp(1)` is `2.71828`   |
| **log(x)**          | Returns the natural logarithm of x.                                                       | `log(2.71828)` is `1.0` |
| **log(x, base)**    | Returns the logarithm of x for the specified base.                                        | `log(100, 10)` is `2.0` |
| **sqrt(x)**         | Returns the square root of x.                                                             | `sqrt(4.0)` is `2`      |
| **hypot(x, y)**     | Returns sqrt(x^2 + y^2).                                                                  | `hypot(3, 4)` is `5.0`  |
| **sin(x)**          | Returns the sine of x. x represents an angle in radians.                                  | `sin(3.14159 / 2)` is `1` |
|                |                                                                                             | `sin(3.14159)` is `0`   |
| **asin(x)**         | Returns the angle in radians for the inverse of sine.                                     | `asin(1.0)` is `1.57`   |
|                |                                                                                             | `asin(0.5)` is `0.523599` |
| **cos(x)**          | Returns the cosine of x. x represents an angle in radians.                                | `cos(3.14159 / 2)` is `0` |
|                |                                                                                             | `cos(3.14159)` is `-1`  |
| **acos(x)**         | Returns the angle in radians for the inverse of cosine.                                   | `acos(1.0)` is `0`      |
|                |                                                                                             | `acos(0.5)` is `1.0472` |
| **tan(x)**          | Returns the tangent of x. x represents an angle in radians.                               | `tan(3.14159 / 4)` is `1` |
|                |                                                                                             | `tan(0.0)` is `0`       |
| **degrees(x)**      | Returns angle in degree for x in radians.                                                | `degrees(1.57)` is `90` |
| **radians(x)**      | Returns angle in radians for x in degrees.                                               | `radians(90)` is `1.57` |


## Strings and Characters

A <span class="code green">string</span> is a sequence of characters. Python treats <span class="code green">strings</span> and <span class="code green">characters</span> the same way.  
Python <span class="code red">does not</span> have a data type for characters.
<span class="code green">Strings</span> must be enclosed in matching:  

*single quotes ( ' ),  
double quotes ( " ),  
or triple-single quotes ( ''' )*.

**Triple single quotes preserve tabs and carriage returns. For example:**

```python
print('''There are three ways to represent strings:
    1. Single quotes,
    2. Double quotes, and
    3. Triple quotes''')
```
Displays:

```console
There are three ways to represent strings:
    1. Single quotes,
    2. Double quotes, and
    3. Triple quotes
```

## The 'ord' and 'chr' Functions

The <span class="code">ord()</span> function returns the <span class="code green">ASCII</span> code for a character.  
The <span class="code">chr()</span> function returns the <span class="code green">character</span> for a given ASCII code.


```python
ch = 'a'
ord(ch)
```
<span class="code">ord(ch)</span> would return the value 97.

```python
chr(97)
```
<span class="code">chr(97)</span> would return the character 'a'.

## Escape Sequences for Special Characters

An <span class="code blue">escape sequence</span> is a special notation that consists of a **backslash ( \ )** followed by a character or combination of digits, which represent a special character.

| Character Escape Sequence | Name            |
|---------------------------|-----------------|
| \b                        | Backspace       |
| \t                        | Tab             |
| \n                        | Linefeed        |
| \f                        | Formfeed        |
| \r                        | Carriage Return |
| \\                        | Backslash       |
| \'                        | Single Quote    |
| \"                        | Double Quote    |

## Printing without the Newline

When using the <span class="code green">print</span> function, a linefeed ( ' \n ' ) is automatically printed.  
By passing a special argument <span class="code blue">end = ""</span>, we can invoke the function to not print anything at the end of the string.

## The 'str' Function

The <span class="code blue">str()</span> function will return a string from an integer.

```python
str(3.4)
```
This function would return <span class="code red">'3.4'</span>

## Concatenation and Repetition Operators

Two strings can be joined with the <span class="code blue">concatenation operator (+)</span>.  
A string can be repeated multiple times with the <span class="code blue">repetition operator (*)</span>.

```python
s1 = "Welcome"
s2 = "Python"
s3 = s1 + " to " + s2
print(s3)
```
```terminal
Welcome to Python
```
```python
s4 = 3 * s1
```
```terminal
WelcomeWelcomeWelcome
```

Augmented assignment operators can also be used for string concatenation.

```python
message = "Welcome to Python"
print(message)
```
```terminal
Welcome to Python
```
```python
message += ". Let's have fun!"
print(message)
```
```terminal
Welcome to Python. Let's have fun!
```

## Reading Strings from Console

The <span class="code blue">input()</span> function reads strings from the console.

## The 'in' and 'not in' Operators

The <span class="code blue">in</span> and <span class="code blue">not in</span> operators test whether a substring is in a string.

```python
s1 = "Welcome
"come" in s1
```
```terminal
True
```
```python
"come" not in s1
```
```terminal
False
```

## Comparing Strings

Strings can be compared with the comparison operators.  
Python compares strings by comparing their corresponding character, and evaluates the characters' numeric codes.

"a" > "A" because the numeric code for "a" is larger than the one for "A".

To compare if <span class="code blue">"Algeria"</span> > <span class="code blue">"Albania"</span>:
1. Compare first characters: "A" == "A"
2. Compare second characters: "l" == "l"
3. Compare second characters: "b" > "g"

"Algeria" is <span class="code red">greater than</span> "Albania".


## Functions for Strings

<span class="code blue">len()</span> returns the number of characters in a string.  
<span class="code blue">max()</span> returns the character with the largest numeric code in a string.  
<span class="code blue">min()</span> returns the character with the smallest numeric code in a string.

## Index Operators '[ ]'

A string is a sequence of characters, an array of characters.  
A character in a string can be accessed through the <span class="code blue">index operator</span> <span class="code green">[]</span>.

```python
s = "ABCDEF"
print(s[0])
```
```terminal
A
```

Python allows negative numbers to reference positions relative to the end of a string.

```python
s = "ABCDEF"
print(s[-1])
```
```terminal
F
```

Strings are also immutable. You cannot change their contents.
For example, this would be illegal:

```python
s[2] = 'A'
```
## The Slicing Operator '[start:end]'

The <span class="code blue">slicing operator [start:end]</span> returns a substring from given start and end positions of a string.

```python
s = "Welcome"
print(s[1:4])
```
```terminal
elc
```

The start or end index may be omitted, which either defaults the starting index to 0, or the end index to len(s) - 1.


## Introduction to Objects and Methods

Every <span class="code blue">datum</span> in Python is an <span class="code green">object</span>.
(e.g. integers, strings)

Every object is assigned a unique, integer <span class="code blue">id</span>, and is defined by a <span class="code blue">class.</span>

For example:
```python
s = "Hello, world!"
```
The <span class="code blue">class</span> of the string variable <span class="code">s</span> is <span class="code">str</span>. <span class="code">  
<class = 'str'></span>  

And it's id could look like:  
<span class="code">505434591</span>

>*In Python, each variable is a reference to an object.*  
>
>*The statement n = 3, assigns value 3 to n, which actually assigns 3 to an int object referenced by variable n.*


You can perform <span class="code green">operations</span> on an object.  
The operations are defined using <span class="code green">functions</span>.  
The functions for objects are called <span class="code green">methods</span>.

## String Methods

Methods are used like the following example:

```python
s = "Hello, world!"
s.capitalize()
```
Whose syntax can be explained like:

><span class="code blue">object</span><span class="code">.</span><span class="code green">method</span><span class="code">()</span>

### String Methods for Searching and Finding Substrings

| Method          | Description                                            |
|-----------------|--------------------------------------------------------|
| **`find()`**        | Searches the string for a specified value and returns the position of where it was found |
| **`rfind()`**       | Searches the string for a specified value and returns the last position of where it was found |
| **`index()`**       | Searches the string for a specified value and returns the position of where it was found |
| **`rindex()`**      | Searches the string for a specified value and returns the last position of where it was found |
| **`startswith()`**  | Returns true if the string starts with the specified value |
| **`endswith()`**    | Returns true if the string ends with the specified value   |

### String Methods for Checking Properties

| Method          | Description                                            |
|-----------------|--------------------------------------------------------|
| **`isalnum()`**     | Returns True if all characters in the string are alphanumeric |
| **`isalpha()`**     | Returns True if all characters in the string are in the alphabet |
| **`isascii()`**     | Returns True if all characters in the string are ASCII characters |
| **`isdecimal()`**   | Returns True if all characters in the string are decimals |
| **`isdigit()`**     | Returns True if all characters in the string are digits     |
| **`isidentifier()`**| Returns True if the string is an identifier         |
| **`islower()`**     | Returns True if all characters in the string are lower case |
| **`isnumeric()`**   | Returns True if all characters in the string are numeric    |
| **`isprintable()`** | Returns True if all characters in the string are printable  |
| **`isspace()`**     | Returns True if all characters in the string are whitespaces |
| **`istitle()`**     | Returns True if the string follows the rules of a title     |
| **`isupper()`**     | Returns True if all characters in the string are upper case |


### String Methods for Case Conversion

| Method          | Description                                            |
|-----------------|--------------------------------------------------------|
| **`capitalize()`**  | Converts the first character to upper case              |
| **`casefold()`**    | Converts string into lower case                          |
| **`lower()`**       | Converts a string into lower case                        |
| **`upper()`**       | Converts a string into upper case                        |
| **`swapcase()`**    | Swaps cases, lower case becomes upper case and vice versa|
| **`title()`**       | Converts the first character of each word to upper case  |

### String Methods for Modification and Replacement

| Method          | Description                                            |
|-----------------|--------------------------------------------------------|
| **`replace(old, new, n)`**     | Returns a string where a specified value is replaced with a specified value (up to n number of times) |
| **`translate()`**   | Returns a translated string                           |
| **`maketrans()`**   | Returns a translation table to be used in translations |

### String Methods for Trimming and Justifying

| Method          | Description                                            |
|-----------------|--------------------------------------------------------|
| **`strip()`**       | Returns a trimmed version of the string                |
| **`lstrip()`**      | Returns a left trim version of the string               |
| **`rstrip()`**      | Returns a right trim version of the string              |
| **`center()`**      | Returns a centered string                               |
| **`ljust()`**       | Returns a left justified version of the string          |
| **`rjust()`**       | Returns a right justified version of the string         |



### String Methods for Encoding and Decoding

| Method          | Description                                            |
|-----------------|--------------------------------------------------------|
| **`encode()`**      | Returns an encoded version of the string               |

### String Methods for Formatting

| Method          | Description                                            |
|-----------------|--------------------------------------------------------|
| **`format()`**      | Formats specified values in a string                   |
| **`format_map()`**  | Formats specified values in a string                   |

### String Methods for Splitting and Joining

| Method          | Description                                            |
|-----------------|--------------------------------------------------------|
| **`split()`**       | Splits the string at the specified separator, and returns a list |
| **`rsplit()`**      | Splits the string at the specified separator, and returns a list |
| **`splitlines()`**  | Splits the string at line breaks and returns a list   |
| **`join()`**        | Converts the elements of an iterable into a string     |
| **`partition()`**   | Returns a tuple where the string is parted into three parts |
| **`rpartition()`**  | Returns a tuple where the string is parted into three parts |

### Other String Methods

| Method          | Description                                            |
|-----------------|--------------------------------------------------------|
| **`count()`**       | Returns the number of times a specified value occurs in a string |
| **`expandtabs()`**  | Sets the tab size of the string                       |
| **`zfill()`**       | Fills the string with a specified number of 0 values at the beginning |






