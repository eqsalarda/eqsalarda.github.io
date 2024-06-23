---
layout: post
title: Chapter 05 - Loops
categories: [COSC1436]
tags: [notes, python]
---

### Contents

1. [The <span class="code">'while'</span> Loop](#the-while-loop)
2. [Loop Design Strategies](#loop-design-strategies)
3. [The <span class="code">'for'</span> Loop](#the-for-loop)

## The 'while' Loop

A <span class="code blue">while</span> loop executes statements for as long as a condition is <span class="code green">true</span>.

Its syntax is as follows:

```python
while(expression):
    Statements
```

A single execution of a loop's body is referred to as a:  
<span class="code blue">iteration</span>


## Loop Design Strategies

### Step 1:
Identify statements that need to be repeated.

### Step 2:
Wrap those statements into a loop.

### Step 3:
Code the loop-continuation-condition.


## The 'for' Loop

A <span class="code blue">for</span> loop in Python, iterates through each value in a sequence.

In general, a <span class="code blue">for</span> loop's syntax is as follows:
```python
for variable in sequence:
    Statements
```

The <span class="code green">range()</span> function is often used as the sequence. Its syntax is as follows:

><span class="code green">range</span><span class="code">(<span class="code red">a</span>, <span class="code red">b</span>, <span class="code red"> c</span>)</span>  

Where <span class="code red">a</span> refers to the starting value,  
which is incremented by <span class="code red">c</span>,  
and limited by <span class="code red">b</span> (not included).

so the function <span class="code">range(0, 8, 2)</span>:  
- will start at the value 0.  
- be incremented by 2.
- until it reaches 8 (not included).

The function would loop a total of 4 times.
- <span class="code">i = 0 , *1*</span>
- <span class="code">i = 2 , *2*</span>
- <span class="code">i = 4 , *3*</span>
- <span class="code">i = 6 , *4*</span>

- <span class="code red">i = 8 , *Not included*</span>

> *The last two arguments are optional.*  
>
> <span class="code green">range(<span class="code red">a</span>)</span>
>
> *will sequence starting at **0**, until <span class="code red">a</span> , and is incremented by 1 by **default***.
