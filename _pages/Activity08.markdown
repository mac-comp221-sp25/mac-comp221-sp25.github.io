---
layout: post
title:  "Activity 08: Sorting as Pre-Processing"
categories: Activity Sorting Design
---

## Learning Goals

You will work towards being able to...

1. Understand sorting as a pre-processing step for solving common algorithmic problems. 

2. Turn algorithmic ideas into pseudocode

## Instructions
Work with your groups on the following problems:

1. **Sorting for Search**: As Skiena tells us, preprocessing an Array with a sorting algorithm lets us use Binary Search instead of Linear Search to find some element. If we only search the array once, is this a good strategy? How many times must we search in order for preprocessing with an $\Theta(n \log n)$ sort to be worth it? Make an argument in terms of Big-Oh time complexities. Note that this is a form of amortized analysis! 

2. **Good-Enough Subset Sum**: Given an array $A$ of Integers and an Integer $k$, find a set $S$ that contains the maximum number of elements in $A$ that sum to less than $k$. For example, If you were given $A = [4, 2, 8, -1, 7]$ and $k = 3$, we should find either $S = \{2, -1\}$ or $S = \{4, -1\}$. Provide pseudocode for a solution and provide an informal analysis of it's time complexity.

3. **Maximum Gap**: Given an array $A$ of Integers, find the pair of Integers $a, b \in A$, $a < b$ such that (1) there is no $c \in A$ such that $a < c < b$ and (2) $\lvert a - b \rvert$ is maximized. That is, find an element $a$ such that the next largest element in $A$, $b$, is as far away as possible. For example, given $A = [4, 2, 1, 14, -7]$, you should find the pair $(4, 10)$. Again, provide pseudocode and an informal analysis of it's time complexity. [^1]

4. If you have extra time, pick a problem described by Skiena 4.1 and write out it's pseudocode. Work through an example with your group. Try and see if you can solve it without sorting first!

#### Submission
Submit an artifact of your work from any of 1--3.  

---

[^1]: This is a variation on LeetCode problem 164! They ask you to do this in *Linear* time & space, which isn't doable with $\Theta(n \log n)$ sort preprocessing, unfortunately. However, the idea is still to preprocess with sorting!
