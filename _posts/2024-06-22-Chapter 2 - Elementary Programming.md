---
layout: post
title: Chapter 02 - Elementary Programming
categories: [COSC1436]
tags: [notes, python]
---

### Contents


1. [Identifiers](#identifiers)
2. [Variables, Assignment Statements, and Expressions](#variables-assignment-statements-and-expressions)
3. [Simultaneous Assignments](#simultaneous-assignment)
4. [Named Constants](#named-constants)
5. [Numeric Data Types and Operators](#numeric-data-types)
7. [Augmented Assignment Operators](#augmented-assignment-operators)
8. [Type Conversions and Rounding](#type-conversions-and-rounding)  
9. [Key Terms](#key-terms)


## Identifiers

<span class="code blue">Identifiers</span> are names of a variable, function, class.

They must follow these rules:
- They must be a sequence of characters that consists of letters, digits, and underscores
- They must start with a letter or underscore
- They cannot be a keyword, or a <span class="code blue">reserved word</span>
- They can be of any length

| Legal Identifier   | Illegal Identifier |
|--------------------|---------------------|
| `variable1`        | `1variable`         |
| `_variable`        | `variable-name`     |
| `variable_name`    | `variable name`     |
| `variableName`     | `for`               |
| `variable123`      | `var!able`          |
| `__init__`         |                     |


## Variables, Assignment Statements, and Expressions

Variables are used to reference values that may be changed in the program.

The statement for assigning a value to a variable is as follows:  

<span class="code blue">variable</span> = <span class="code green">expression</span>

```python
a = 1
b = a + 1
c = b + a + 3
sumLetters = a + b + c
```

The **scope** of a variable refers to where, in the program, a variable can be used.  
A variable must be created before it can be used.

```python
count = count + 1       # Must be defined first.
```
An error will occur if <span class="code">'count'</span> is not defined before the expression.
```python
count = 0               # Assign count to 0.
count = count + 1       # Add 1 to count.
```
## Simultaneous Assignment

Python supports <span class="code blue">simultaneous assignment</span> in syntax like this:
```python
var1, var2, ..., varn = exp1, exp2, ..., expn
```
This tells Python to evaluate all the expressions on the right, and assign them to their corresponding variable <span class="code green">simultaneously.</span>

Example of swapping variables in C vs Python:  

<span class="code">C:</span>

```c
int x = 1;
int y = 2;
int temp = 0;

temp = y;
y = x;
x = temp;
```

<iframe style="border:none" width="100%" height="250" src="https://whimsical.com/embed/U2MMT2GgHL54V4xrSHx9zC"></iframe>

<span class="code">Python:</span>

```python
x = 1
y = 2
x, y = y, x
```

<iframe style="border:none" width="100%" height="250" src="https://whimsical.com/embed/AoiJkDgZUgHiCqnM1ua2Tt"></iframe>

## Named Constants

A <span class="code blue">named constant</span> represents permanent data that never changes.  
In this code:
```python
# Assign a radius
radius = 20

# Compute area
PI = 3.14159
area = radius * radius * PI

# Display results
print("The area for the circle of radius", radius, "is", area)
```

<span class="code">'PI'</span> is a constant with an assigned value of 3.14159.

Benefits of Constants:
1. Avoid repetitive typing of the same value.
2. Easy value changes from a single location.

## Numeric Data Types and Operators

#### Numeric Data Types

Python has two numeric types:
1. Integers: Whole numbers
2. Real numbers: Numbers with fractional parts.

Real numbers are represented as <span class="code blue">floating-point</span> values, also known as <span class="code blue">floats.</span>

A <span class="code blue">literal</span> is a constant value that appears directly in a program.

> By default, an integer literal is a decimal integer number.  
> To denote a binary integer literal, lead the number with 0B.  
> To denote a hexadecimal integer literal, lead the number with 0X  
```python
print(0B1111) # Displays 15
print(0XFFFF) # Displays 65535
```

Python also allows you to use underscores to separate digits in a number literal.

```python
value = 1_000_000
amount = 24.24_25_26
```
<span class="code">'value'</span> would equal 1,000,000.  
<span class="code">'amount'</span> would equal 24.242526.

#### Operators

| Name            | Meaning          | Example      | Result |
|-----------------|------------------|--------------|--------|
| `+`             | Addition         | `34 + 1`     | 35     |
| `-`             | Subtraction      | `34.0 − 0.1` | 33.9   |
| `*`             | Multiplication   | `300 * 30`   | 9000   |
| `/`             | Float division   | `1 / 2`      | 0.5    |
| `//`            | Integer division | `1 // 2`     | 0      |
| `**`            | Exponentiation   | `4 ** 0.5`   | 2      |
| `%`             | Remainder        | `20 % 3`     | 2      |

<span class="code blue">Unary</span> operators have 1 single operand. (e.g. The negative sign in ' -5 ' )  
<span class="code blue">Binary</span> operators have 2. (e.g. The minus sign in ' 4 - 5 ' )

The <span class="code">'/'</span> operator performs a float division that results in a floating-point number.  

The <span class="code">'//'</span> operator performs an integer division that truncates any fractional part of a number.  

The <span class="code">'**'</span> operator exponentiates the 1st operand by the 2nd operand.

The <span class="code">'%'</span> operator yields the remainder after division.

## Augmented Assignment Operators

| Operator | Name                    | Example      | Equivalent  |
|----------|-------------------------|--------------|-------------|
| `+=`     | Addition assignment     | `i += 8`     | `i = i + 8` |
| `-=`     | Subtraction assignment  | `i -= 8`     | `i = i - 8` |
| `*=`     | Multiplication assignment| `i *= 8`    | `i = i * 8` |
| `/=`     | Float division assignment| `i /= 8`    | `i = i / 8` |
| `//=`    | Integer division assignment| `i //= 8` | `i = i // 8`|
| `%=`     | Remainder assignment    | `i %= 8`     | `i = i % 8` |
| `**=`    | Exponent assignment     | `i **= 8`    | `i = i ** 8`|

## Type Conversions and Rounding

```python
value = 5.6
int(value)
```
In this code, <span class="code">'value'</span> will equal 5.  
Note that the fractional part is truncated, rather than rounded.

```python
value = 5.6
round(value)
```
In this code <span class="code">'value'</span> will equal 6.

## Key Terms

<span class="code blue">algorithm</span>  
&nbsp;&nbsp;&nbsp;&nbsp;Statements that describe how a problem is solved in terms of the actions to be executed, and specifies the order in which these actions should be executed.  
<span class="code blue">assignment operator</span>  
&nbsp;&nbsp;&nbsp;&nbsp;(=) The operator that assigns values to variables.  
<span class="code blue">camelCase</span>  
&nbsp;&nbsp;&nbsp;&nbsp;A convention for naming variables and functions. If a name consists of several words, lowercase the first word, and uppercase the first letter of every subsequent word.  
<span class="code blue">data type</span>  
&nbsp;&nbsp;&nbsp;&nbsp;The type for a value such as integers or strings.  
<span class="code blue">expression</span>  
&nbsp;&nbsp;&nbsp;&nbsp;A representation of computation involving values, variables, and operators, which evaluates to a value.   
<span class="code blue">floating-point number</span>  
&nbsp;&nbsp;&nbsp;&nbsp;A number with a fractional part.  
<span class="code blue">identifier</span>  
&nbsp;&nbsp;&nbsp;&nbsp;A name of a variable, function, class.  
<span class="code blue">incremental development and testing</span>  
&nbsp;&nbsp;&nbsp;&nbsp;A programming methodology that develops and tests programs incrementally. It helps eliminate errors by isolating them.  
<span class="code blue">input-process-output (IPO)</span>  
&nbsp;&nbsp;&nbsp;&nbsp;The essence of system analysis and design.  
<span class="code blue">keyword</span>  
&nbsp;&nbsp;&nbsp;&nbsp;(or reserved word) Words which have specific meaning to the compiler and cannot be used for other purposes in a program.  
<span class="code blue">line continuation symbol</span>  
&nbsp;&nbsp;&nbsp;&nbsp;( \ ) Indicates to the interpreter that a statement is continued on the next line.  
<span class="code blue">literal</span>  
&nbsp;&nbsp;&nbsp;&nbsp;A constant value that appears directly in the program.  
<span class="code blue">operand</span>  
&nbsp;&nbsp;&nbsp;&nbsp;The values operated on by an operator.  
<span class="code blue">pseudocode</span>  
&nbsp;&nbsp;&nbsp;&nbsp;Natural language mixed with code.  
<span class="code blue">requirements specification</span>  
&nbsp;&nbsp;&nbsp;&nbsp;A formal process that seeks to understand a problem that software will address, and to document what the software system needs to do.  
<span class="code blue">reserved word</span>  
&nbsp;&nbsp;&nbsp;&nbsp;(keyword)  
<span class="code blue">scope of a variable</span>  
&nbsp;&nbsp;&nbsp;&nbsp;The portion of a program where the variable can be accessed.  
<span class="code blue">simulataneous assignment</span>  
&nbsp;&nbsp;&nbsp;&nbsp;Assign multiple values to multiple variables in one statement.  
<span class="code blue">system analysis</span>  
&nbsp;&nbsp;&nbsp;&nbsp;Seeks to analyze data flow and to identify a system's input and output.  
<span class="code blue">system design</span>  
&nbsp;&nbsp;&nbsp;&nbsp;Stage where programmers develop a process for obtaining the output from the input.  
<span class="code blue">type conversion</span>  
&nbsp;&nbsp;&nbsp;&nbsp;Conversion from one data type to another.  
<span class="code blue">variable</span>  
&nbsp;&nbsp;&nbsp;&nbsp;Used to store data in the program.  