## Chapter 06: Functions

### Contents

1. [Defining a Function](#defining-a-function)
2. [Calling a Function](#calling-a-function)
3. [Return Values](#return-values)
4. [Positional and Keyword Arguments](#positional-and-keyword-arguments)
5. [Passing Arguments by Reference Values](#passing-arguments-by-reference-values)
6. [Modularizing Code](#modularizing-code)
7. [Variable Scope](#variable-scope)
8. [Default Arguments](#default-arguments)
9. [Returning Multiple Values](#returning-multiple-values)
10. [Abstraction and Stepwise Refinement](#abstraction-and-stepwise-refinement)

## Defining a Function

The syntax for defining a <span class="code blue">function</span> is as follows:

```python
def functionName(parameters):
    # Function Body
```
A function contains a <span class="code">header</span>, beginning with the <span class="code">def</span> keyword and a list of the function's <span class="code green">parameters</span>.

Parameters are like *placeholders*.
When you call a function with values in place of a parameter, the values are refered to as <span class="code red">arguments</span>.

```python
def functionName(parameter1, parameter2) # Placeholders
    # blah blah blah


z = functionName(argument1, argument2) # Values in place of arguments, like 1, 2, 3
```
> *A function can return a value using the <span class="code">return</span> key word*
>
> *If a function returns a value, it is called a <span class="code green">value-returning function</span>.*



## Calling a Function

A function is called by *invoking* its name.

Here are some examples of how and where functions can be called:

```python
def main():
    blah blah
def max():
    blah blah
def min():
    blah blah

main() # Functions can be called on its own
max = max() # Functions can be treated as *expressions* if they return a value
print(min()) # Functions can be called within other functions.
```


## Return Values

If a function has no return value, it is referred to as a <span class="code blue">void function</span>.

The function <span class="code blue">def</span> <span class="code">main()</span> often does not have a return value.


## Positional and Keyword Arguments



## Passing Arguments by Reference Values



## Modularizing Code



## Variable Scope



## Default Arguments



## Returning Multiple Values



## Abstraction and Stepwise Refinement
