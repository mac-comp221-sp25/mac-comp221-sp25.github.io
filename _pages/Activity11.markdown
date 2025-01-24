---
layout: post
title:  "Activity 11: The Master Theorem"
categories: Activity Sorting Design
---

## Learning Goals

You will work towards being able to...

1. State the definition of the Master Theorem   

2. Determine the runtime complexity of recursive functions

3. Use the Master Theorem to understand when a divide and conquer approach results in a faster algorithm 

## Instructions
Work with your groups to draw trees that trace the recursive structure of algorithms with the following recurrence relations. For example, for MergeSort, our structure would look something like the below image

<img src="{{ site.url }}/assets/imgs/recursion.png" width="300" />

Each number represents the time complexity of everything but the recursion for that call, and that node's children represent the recursive calls made from that call. Note that we work out the height of our tree (how many recursions until our problem size is 1?) and the number of leaves in our tree (after all of our recursions, how many branches do we create?). Then observe that the sum of all of these runtimes is our *total* runtime! 

As you draw and analyze each tree, pay attention to which terms will dominate the total runtime. Then compare your findings to the master theorem

1. $T(n) = 2T(\frac{n}{3}) + n^2$

2. $T(n) = 3T(\frac{n}{2}) + n$

3. $T(n) = 4T(\frac{n}{2}) + n^2$

#### Submission
Submit an artifact of your work from either 1 or 2 or 3.

