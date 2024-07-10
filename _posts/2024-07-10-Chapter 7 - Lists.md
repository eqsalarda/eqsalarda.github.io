---
layout: post
title: Chapter 07 - Lists
categories: [COSC1436]
tags: [notes, python]
---

### Contents


- [List Basics](#list-basics)
- [List is a Sequence](#list-is-a-sequence)
- [Functions for Lists](#functions-for-lists)
- [The Index Operator](#the-index-operator)
- [List Slicing](#list-slicing)
- [The +, +=, *, and in/not in Operators](#the--+-=-*-and-innot-in-operators)
- [Traversing Elements in a For Loop](#traversing-elements-in-a-for-loop)
- [Comparing Lists](#comparing-lists)
- [List Comprehensions](#list-comprehensions)
- [List Methods](#list-methods)
- [Splitting a String into a List](#splitting-a-string-into-a-list)
- [Inputting Lists](#inputting-lists)
- [Shifting Lists](#shifting-lists)
- [Copying Lists](#copying-lists)
- [Searching Lists](#searching-lists)
- [Sorting Lists](#sorting-lists)


## List Basics

To create a list, use the following syntax:
```python
list1 = [] # Creates an empty list.
list2 = [2,3,4] # Creates a list with elements 2, 3, 4.
list3 = ["red", "green"] # Creates a list with strings.
list4 = list(range(3,6)) # Creates a list with elements 3, 4, 5.
list5 = list("abcd") # Creates a list of elements a, b, c, d.
```
Elements in a list are enclosed with brackets and separated by commas.  

A list can contain elements of mixed types. For example:

```python
listmixed = [1, "red", 4.1]
```
In this example, <span class="code">listmixed</span> is a valid list.


## List is a Sequence

Just as strings are simply a sequence of characters, a list is a sequence of any kind of element.

Here is a list of common operations for lists:

| Operation           | Description                                                  |
|---------------------|--------------------------------------------------------------|
| `x in s`            | True if element x is in sequence s.                          |
| `x not in s`        | True if element x is not in sequence s.                      |
| `s1 + s2`           | Concatenates two sequences s1 and s2.                        |
| `s * n`, `n * s`    | n copies of sequence s concatenated.                         |
| `s[i]`              | ith element in sequence s.                                   |
| `s[i : j]`          | Slice of sequence s from index i to j–1.                     |
| `len(s)`            | Length of sequence s, i.e., the number of elements in s      |
| `min(s)`            | Smallest element in sequence s.                              |
| `max(s)`            | Largest element in sequence s.                               |
| `sum(s)`            | Sum of all numbers in sequence s.                            |
| `for loop`          | Traverses elements from left to right in a for loop.         |
| `<, <=, >, >=, ==, !=` | Compares two sequences.                                   |


## Functions for Lists

There are several built-in functions for lists in Python.

| Function         | Description                                                                        |
|------------------|------------------------------------------------------------------------------------|
| `len()`          | Returns the number of elements in the list.                                        |
| `max()`          | Returns the element with the greatest value in the list.                           |
| `min()`          | Returns the element with the lowest value in the list.                             |
| `sum()`          | Returns the sum of all elements in the list.                                       |
| `random.shuffle()` | Shuffles the elements randomly in the list (from the `random` module).          |



## Index Operator '[ ]'

An element in a list can be accessed through the index operator, using the following syntax:

```python
myList[index]
```
Where <span class="code">index</span> contains the numerical position of the element's index.

Indexed elements can be used just like a variable. For example:

```python
myList[2] = myList[0] + myList[1]
```

This code adds the values of the first and second index of <span class="code">myList</span> and assigns it to the list's third index.


## List Slicing

The slicing operator returns a "slice" of a list, using the following syntax:

```python
myList[start : end : step]
```

Here's an example of how it is used:

```python
myList = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
print("Output: ", end="")
print(myList[2:4])
```
```sh
Output: 2, 3, 4
```

You can also use negative indexes which will reference the end position of a list, rather than the beginning.



## The +, +=, *, and in/not in Operators

<span class="code blue">Concatenation ( + )</span>  

**Example 1:**
```python
list1 = [1, 2, 3]
list2 = [4, 5, 6]
list3 = list1 + list2
print(list3)
```
```sh
[1, 2, 3, 4, 5, 6]
```
**Example 2:**

```python
list1 = [1, 2, 3]
list1 += [4, 5]
print(list1)
```
```sh
[1, 2, 3, 4, 5]
```

<span class="code blue">Repetition Operator ( * )</span>
```python
list1 = [1, 2, 3]
list2 = list1 * 3
print(list2)
```
```sh
[1, 2, 3, 1, 2, 3, 1, 2, 3]
```
<span class="code blue">'in' and 'not in' Operators</span>

```python
list1 = [1, 2, 3, 4, 5]
check1 = 1 in list1
check2 = 1 not in list1
check3 = 6 in list1
check4 = 6 not in list1
print(check1, check2, check3, check4)
```
```sh
True False False True
```


## Traversing Elements in a For Loop

The elements in a Python list are iterable.  

For example:

```python
for u in myList:
    print(u)
```
This code displays all the elements in the list <span class="code">myList</span>.

This code can be read as:
> For each element <span class="code">u</span> in <span class="code">myList</span>, print it.

## Comparing Lists

Comparison operators are used to compare lists.  
Lists must be of the same type in order to be comparable.  

These comparisons use <span class="code red">lexicographical ordering</span>.

Lexicographical ordering in terms of list comparisons refers to the way lists are compared element by element in the same manner as words are compared in a dictionary. This comparison follows these rules:

1. **Element-wise Comparison**: Lists are compared element by element from the first to the last.
2. **First Unequal Element**: The comparison is determined by the first pair of elements that are not equal. The list with the smaller element in this pair is considered smaller.
3. **Length Consideration**: If one list is a prefix of the other, the shorter list is considered smaller.
4. **Natural Order**: Elements are compared using their natural order (for numbers, this is numerical; for strings, this is alphabetical).

For example:
- `[1, 2, 3] < [1, 2, 4]` because the first differing elements are `3` and `4`, and `3 < 4`.
- `['apple', 'banana'] < ['apple', 'cherry']` because the first differing elements are `'banana'` and `'cherry'`, and `'banana' < 'cherry'` lexicographically.
- `[1, 2] < [1, 2, 0]` because the first list is shorter and the elements are the same up to the length of the first list.

In Python, this behavior is implemented using the comparison operators `<`, `<=`, `>`, `>=`, `==`, and `!=` for lists.

## List Comprehensions

A list comprehension involves brackets containing an expression, followed by a <span class="code">for</span> clause and/or more <span class="code">for</span> clauses or <span class="code">if</span> clauses.

```python
list1 = [x for x in range(5)] # Returns a list of 0, 1, 2, 3, 4
```

## List Methods

| Method               | Description                                                                                                                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `append(x)`          | Adds an element x to the end of the list.                                                                                                                                                                                   |
| `count(x)`           | Returns the number of times element x appears in the list.                                                                                                                                                                  |
| `extend(anotherList)`| Appends all the elements in anotherList to the list.                                                                                                                                                                        |
| `index(x)`           | Returns the index of the first occurrence of element x in the list.                                                                                                                                                         |
| `insert(index, x)`   | Inserts an element x at a given index. Note that the first element in the list has index 0.                                                                                                                                  |
| `pop(index)`         | Removes the element at the given index and returns it. The parameter index is optional. If it is not specified, `list.pop()` removes and returns the last element in the list.                                             |
| `remove(x)`          | Removes the first occurrence of element x from the list.                                                                                                                                                                    |
| `reverse()`          | Reverses the elements in the list.                                                                                                                                                                                          |
| `sort()`             | Sorts the elements in the list in ascending order.                                                                                                                                                                          |

## Splitting a String into a List

To split characters in a string, use:
```python
list("abcdefg")
```
Which returns:
```sh
[a, b, c, d, e, f, g]
```
To split strings based on specified characters, use:
```python
letters = "ABC DEF GHI JKL".split()
```
Which returns:
```sh
["ABC", "DEF", "GHI", "JKL"]
```
You can pass arguments into the <span class="code">split()</span> method, indicating where to split the string.

```python
date = "07/10/2024"
list = date.split("/")
```
Which returns:
```sh
["07", "10", "2024"]
```


## Inputting Lists

Reading data from console into a list can be accomplished in the following ways:

```python
list1 = []
for i in range(10):
    list1.append(input("Enter input: "))
```
Or:
```python
x = input("Enter input separated by spaces: ")
items = x.split()
list1 = [i for i in items]
```

## Copying Lists

To copy data in one list to another, you must copy individual elements from the source to the destination list.

In this example:
```python
list2 = list1
```
<span class="code">list2</span> does not contain the contents of <span class="code">list1</span> but rather, is a <span class="code green">reference</span> to <span class="code">list1.</span>

Acquiring a copy of a list can be achieved by the following:

```python
list2 = [x for x in list1] # 1st example
list2 = [] + list1 # 2nd example
list2 = list1[ : ] # 3rd example
```