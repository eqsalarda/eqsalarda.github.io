---
layout: post
title: Chapter 03 - Selections
categories: [COSC1436]
tags: [notes, python]
---

### Contents

1. [Boolean Types, Values, and Expressions](#boolean-types-values-and-expressions)
2. [Generating Random Numbers](#generating-random-numbers)
3. [if Statements](#if-statements)
4. [Two-Way if-else Statements](#two-way-if-else-statements)
5. [Nested if and Multi-Way if-elif-else Statements](#nested-if-an-multi-way-if-elif-else-statements)
6. [Common Errors in Selection Statements](#common-errors-in-selection-statements)
7. [Logical Operators](#logical-operators)
8. [Conditional Expressions](#conditional-expressions)
9. [match-case Statements](#match-case-statements)
10. [Operator Precedence and Associativity](#operator-precedence-and-associativity)
11. [Chapter Summary](#chapter-summary)

## Boolean Types, Values, and Expressions
A *boolean expression* is an expression that evaluates to <span class="code green">True</span> or <span class="code red">False</span>.

| Python Operator | Mathematics Symbol | Name                  |
|-----------------|--------------------|-----------------------|
| `<`             | <                  | less than             |
| `<=`            | ≤                  | less than or equal to |
| `>`             | >                  | greater than          |
| `>=`            | ≥                  | greater than or equal to |
| `==`            | =                  | equal to              |
| `!=`            | ≠                  | not equal to          |

> <span class="code">Note: '==' tests for equality.  '=' is used for assignment.</span>
```python
radius = 1
print(radius > 0)
```
The result of the comparison is a <span class="code blue">Boolean value</span>: <span class="code green">True</span> or <span class="code red">False</span>.  
In this example, <span class="code green">True</span> would be printed out to us.
```python
lightsOn = True
```
A variable that holds a boolean value is called a <span class="code blue">boolean variable</span>.  

True and False are literals, like the number '10'. They cannot be used as identifiers in a program.

## Generating Random Numbers
```python
random.randint(a,b)
```
The <span class="code">randint(a, b)</span> function can be used to generate a random integer <span class="code blue">between</span> <span class="code">a</span> and <span class="code">b</span> respectively. 

This function is within the <span class="code">random</span> module. To obtain a random integer between 0 and 9, use:
```python
import random

number = random.randint(0, 9)
```

The endpoints of the function are **inclusive**.  
So in this example, 0 and 9 can be randomly generated.

```python
random.randrange(0, 9)
```
<span class="code blue">randrange(a, b)</span> generates a random integer between <span class="code blue">a</span> and <span class="code blue">b - 1</span>. 

```python
random.random()
```
<span class="code blue">random.random()</span> generates a random <span class="code green">float</span> value between 0.0 and 1.0, <span class="code red">excluding</span> 1.0.


## if Statements
An if statement is a construct that enables a program to specify an alternative path of execution.

### One-Way if Statements
```python
if (boolean expression here):
    Statements
```
><span class="code">Note: Statements that belong to an if statement must be indented at least one space to the right of the <span class="code blue">if</span> keyword.</span>

<iframe style="border:none" width=100% height="250" src="https://whimsical.com/embed/KdKynsHayUDcGjsVvKwu3D"></iframe>


## Two-Way if-else Statements
```python
if (boolean expression here):
    Statements when true
else:
    Statements when false
```
A two-way <span class="code blue">if-else</span> statement decides the execution path based on whether or not a condition is true or false.

<iframe style="border:none" width=100% height="250" src="https://whimsical.com/embed/BM3DA1wL1j763nCsWYoEfL"></iframe>


## Nested if an Multi-Way if-elif-else Statements
```python
if score >= 90.0:
    print("grade is A")
else:
    if score >= 80.0:
        print("grade is B")
    else:
        if score >= 70.0:
            print("grade is C")
        else:
            if score >= 60.0:
                print("grade is D")
            else:
                print("grade is F")
```

If statements can be placed within themselves. This can be used to implement different alternatives. In this example, we assign a letter grade according to the score.

## Common Errors in Selection Statements
Most common errors in selection statements are caused by indentation errors.
```python
radius = -20

if radius >= 0:
    area = radius * radius * 3.14
print("The area is", area)
```
<span class="code red">The print statement is not inside the if statement.</span>

```python
radius = -20

if radius >= 0:
    area = radius * radius * 3.14
    print("The area is", area)
```
<span class="code green">The program will now print the area when the radius is >= 0.</span>

## Logical Operators
The logical operators <span class="code blue">not, and, or,</span> can be used to create compound boolean expressions.

| Operator | Description          |
|----------|----------------------|
| `not`    | logical negation     |
| `and`    | logical conjunction  |
| `or`     | logical disjunction  |

## Conditional Expressions




## match-case Statements


## Operator Precedence and Associativity


## Chapter Summary








