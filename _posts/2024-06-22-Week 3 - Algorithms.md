---
layout: post
title: Week 3 - Algorithms
categories: [CS50x]
tags: [notes, C]
---

### Contents

1. [Linear Search](#linear-search)

2. [Binary Search](#binary-search)

3. [Running Time](#running-time)

4. Data Structures

5. Sorting

6. Bubble Sort

7. Recursion

8. Merge Sort

## Linear Search

Linear search is an algorithm used to find a particular value in a list.

It checks each value in a list, sequentially until the desired element is found.

### Time Complexity

- Best Case: This occurs when the element is first in the list. $$ O(1) $$

- Worst Case: This occurs when the element is last in the list. $$ O(n) $$

- Average Case: $$ O(n) $$

```c
int linearSearch(int array[], int size, int target)
{
    for (int i = 0; i < size; i++)
    {
        if (array[i] == target)
        {
            printf("Target found.");
            return i;
        }
    }
}
```
This code is an implementation of linear search as it checks every index in <span class="code">array[]</span>, and returns the index it found the target in.

## Binary Search

Binary search is a highly efficient algorithm for finding an element in a **sorted** array.

It functions by repeatedly dividing the search interval in half, and comparing the middle value to the target element.

### Time Complexity

- Best Case: This occurs when the target is the middle element of the array. $$ O(1) $$

- Worst Case:  $$ O(log (n)) $$

- Average Case: $$ O(log (n)) $$

```c
int binarySearch(int arr[], int size, int target) {
    int left = 0;
    int right = size - 1;
    
    while (left <= right) {
        int mid = left + (right - left) / 2;

        // Check if the target is present at mid
        if (arr[mid] == target) {
            return mid;
        }

        // If the target is greater, ignore the left half
        if (arr[mid] < target) {
            left = mid + 1;
        }
        // If the target is smaller, ignore the right half
        else {
            right = mid - 1;
        }
    }

    // Target is not present in the array
    return -1;
}
```

## Running Time

