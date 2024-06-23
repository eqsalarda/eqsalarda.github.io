---
layout: post
title: Week 2 - Arrays
categories: [CS50x]
tags: [notes, C]
---

### Contents

1. [Arrays](#arrays)

2. [Strings](#strings)

3. [Command-Line Arguments](#command-line-arguments)

## Arrays

An array is a collection of elements, all of the same type, stored in contiguous memory locations.  
Arrays allow you to store multiple values in a single variable, making for easier management.

The declaration of an array is as follows:

<span class="code blue">type</span> <span class="code">arrayName[<span class="code green">arraySize</span>];</span>

```c
int numbers[10];
```
This code declares an array <span class="code">'numbers'</span> of 10 integers.

If the size of an array is not specified, it is determined by the number of elements in the initializer.

```c
int numbes[] = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9};
```
### Accessing Elements

Elements of an array are accessed using the index, which stats at 0.

```c
int firstElement = numbers[0];
numbers[2] = 10;
```
The integer variable <span class="code">'firstElement'</span> is assigned the value of the first element, index 0, in the array <span class="code">'numbers'</span>.  
Then, the element at index <span class="code">[2]</span> is assigned the value of 10.

### Multidimensional Arrays

Multidimensional arrays in C are 'arrays of arrays.'  
They allow for the creation of tables, matricies, and other structures that require multiple indicies to access individual elements.

They are declared as follows;

<span class="code blue">type</span> <span class="code">arrayName[<span class="code green">size1</span>][<span class="code green">size2</span>]...[<span class="code green">sizen</span>];</span>

### Array Size

The size of an array can be retrieved using the <span class="code">'sizeof'</span> operator, which gets the size of the array in bytes.

```c
int numbers[10];
size_t size = sizeof(numbers);
```

### Passing Arrays to Functions

Arrays are passed to functions by reference, not by value.

```c
void printArray(int arr[], int size)
{
    for (int i = 0; i < size; i++)
    {
        printf("%d", arr[i]);
    }
    printf("\n");
}
```

### Important Points

#### Bounds Checking

C does not perform bounds checks. Accessing an array out of its bounds leads to undefined behavior.

#### Pointer Arithmetic

The name of the array is a pointer to its first element.

```c
int numbers[10];
int firstElement = *numbers;
int secondElement = *(numbers + 1);
```
## Strings

Strings in C are arrays of characters terminated by a null character <span class="code">'\0'</span>.

Character Array:

```c
char str[] = "Hello, World!";
```
- Storage: The string is stored as an array on the stack.
- Modifiability: This array is modifiable. <span class="code">'str[0] = 'h';</span> is valid.


Pointer to String Literal:
```c
char *str = "Hello, World!";
```
- Storage: The string is stored in a read-only section of memory.
- Modifiability: This array is not modifiable. <span class="code">'str[0] = 'h';</span> will often lead to a segmentation fault.

## Command-Line Arguments

Command-line arguments provide a way to pass information when a program is started.  

This can be helpful for configuring a program's behavior without changing the source code.

They are accessed through the <span class="code">'main'</span> function's parameters: <span class="code blue">int</span><span class="code"> argc</span> and <span class="code blue">char *</span><span class="code">argv[]</span>.

```c
#include <stdlib.h>
#include <stdio.h>

int main(int argc, char *argv[])
{
    if (argc != 2)
    {
        printf("Usage: ./program [arguments]");
        return 1;
    }
    
    int numb1 = atoi(argv[1]);
    int function(argv[1]);
    return 0;
}
```
- <span class="code blue">int</span><span class="code"> argc</span> - Argument Count  
-&nbsp;&nbsp;&nbsp;&nbsp;This represents the number of command-line arguments passed to the program itself.
- <span class="code blue">char *</span><span class="code">argv[]</span> - Argument Vector  
-&nbsp;&nbsp;&nbsp;&nbsp;This array represents the arguments themselves.

In this code, if there are more than 2 arguments passed to the program, an error code is returned, and proper usage is communicated to the user.  

The argument in <span class="code blue">argv[1]</span> is then converted to an integer from a string, and passed as a parameter to function <span class="code">'function'</span>.

```sh
./program argument
```
It is important to note that <span class="code blue">argv[0]</span> will contain the name of the program, and <span class="code blue">argv[1]</span> to <span class="code blue">argv[argc - 1]</span> will contain the actual command-line arguments.

